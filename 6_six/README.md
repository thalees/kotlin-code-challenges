# Problem Name

![image](https://user-images.githubusercontent.com/40672950/77836861-afd06980-7138-11ea-9b07-5565a280a13d.png)
**CodeForce:** https://codeforces.com/contest/1297/problem/F

---

## Solução 🇧🇷

A observação principal é a seguinte: quando escolhemos quais filmes assistir, o ideal é escolher aqueles cujos _bi_ são mínimos possíveis. Isso pode ser comprovado por contradição:

- suponha que tenhamos a resposta onde _ti > tj_ porém _bi < bj_, vamos trocar _ti_ e _tj_ e obter:
> max (bi-tj, bj-ti) ≤ max (bi-ti, bj-tj) - a contradição.

Agora, vamos simular cuidadosamente o processo. Vamos iterar ao longo do dia **D** e manter um conjunto de segmentos [ai,bi] (onde _ai ≤ D_) classificados por _bi_.

Assim, podemos fazer o seguinte: para um **D** fixo, primeiro, vamos adicionar ao conjunto todos os segmentos [ai,bi] com _ai = D_. Em seguida, escolha _min (m, tamanho definido)_ filmes que assistiremos no dia **D**. E, finalmente, se o aparelho não estiver vazio, passe de **D** para **D+1**. Caso contrário, vamos passar **D** direto para o próximo evento.

Como existem _O(n)_ eventos e _O(n)_ filmes, pode-se provar que verificamos apenas _O(n)_ dias e haverá _O(n)_ dias e haverá _O(n)_ "first ()" e "remove () "consultas ao conjunto. Portanto, a complexidade total é **O(nlog (n))**.

---

## Solution 🇬🇧

The key observation is the following: when we choose which movies to watch, it's optimal to choose ones whose _bi_ are minimal possible. It can be proven by contradiction: suppose we have the answer where _ti > tj_ but _bi < bj_, let's swap _ti_ and _tj_ and get:
> max(bi−tj,bj−ti) ≤ max(bi−ti,bj−tj) — the contradiction.

Now, let's carefully simulate the process. Let's iterate over day **D** and maintain a set of segments [ai,bi] (where _ai ≤ D_) sorted by _bi_.

So we can do the following: for a fixed **D**, at first, let's add to the set all segments [ai,bi] with _ai = D_. Then choose _min( m, set size)_ movies we will watch at day **D**. And finally, if the set is not empty then move from **D** to **D+1**. Otherwise, let's move **D** straight to the next event.

Since there are _O(n)_ events and _O(n)_ movies it can be proven that we will check only _O(n)_ days and there will be _O(n)_ "first()" and "remove()" queries to the set. So, the total complexity is **O(nlog(n))**.
