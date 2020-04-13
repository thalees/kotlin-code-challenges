# Problem Name

![image](https://user-images.githubusercontent.com/40672950/77836861-afd06980-7138-11ea-9b07-5565a280a13d.png)
**CodeForce:** https://codeforces.com/contest/1297/problem/H

---

## Solução 🇧🇷

Suponha (sem perda de generalidade) que a primeira letra **s0** pertença à string **r**. Para descobrir algumas propriedades da resposta ideal, vejamos a seguinte situação: o prefixo de comprimento _i_ de s pertence a **r** (portanto, _b_ está vazio) e decidimos onde colocar _si_.

Se _si> r0_, é ideal adicioná-lo em _r_, já que _max (r + si, "") <max (r, si) _. Se _si <r0_, é ideal adicionar todo o sufixo _si ... s | s | −1_ em _b_ desde que _si ... s | s | −1 <r_ e _r <r + (qualquer letra)_.

O único caso é _si = r0_ e aqui devemos verificar as duas variantes. Mas se adicionarmos _si_ a _b_, podemos "largar" as primeiras letras em _r_ e _b_. Portanto, podemos ver que, em qualquer caso, o seguinte padrão será válido:
> s = ps + ss, r ⊆ ps eb = (prefixo de r) + ss (é claro, r ≥ b).

Então, podemos escrever **dp[i][j]**, onde _i_ é o comprimento do prefixo _ps_ e _j_ é o comprimento da primeira parte de _b_, que é um prefixo de _r_. O valor de _dp_ é a cadeia lexicograficamente mínima _r_, se existir.

As transições são naturais: para **dp[i][j]**, podemos tentar adicionar _si_ a _r_ ou a _b_, se possível. O mínimo possível _r_ é **dp[n][j]** para alguns _j_ ou **dp[i][j]** se _si <rj_.

A complexidade resultante é _O(t x n3)_, mas com um fator constante bastante pequeno.

---

## Solution 🇬🇧

Suppose (without loss of generality) the first letter **s0** belongs to string **r**. To find out some properties of the optimal answer, let's look at the following situation: the prefix of length _i_ of s belongs to **r** (so, _b_ is empty) and we decide where to put _si_.

If _si > r0_ then it's optimal to add it in _r_ since _max(r+si,"") < max(r,si)_. If _si < r0_ then it's optimal to add all suffix _si...s|s|−1_ in _b_ since _si...s|s|−1 < r_ and _r < r+(any letters)_.

The only case is _si = r0_ and here we should check both variants. But if we add _si_ to _b_ we can "drop" first letters both in _r_ and _b_. So we can see that in any case, the following pattern will hold:
> s = ps + ss, r ⊆ ps and b = (prefix of r) + ss (of course, r ≥ b).

So we can write **dp[i][j]**, where _i_ is the length of the prefix _ps_ and _j_ is the length the first part of _b_ which is a prefix of _r_. The value of _dp_ is the lexicographically minimum string _r_ if it exists.

The transitions are natural: for **dp[i][j]** we can try to add _si_ either to _r_ or to _b_ if possible. The minimal possible _r_ is either **dp[n][j]** for some _j_ or **dp[i][j]** if _si < rj_.

The resulting complexity is _O(t x n3)_ but with quite a small constant factor.
