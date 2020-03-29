
# Problem Name

![image](https://user-images.githubusercontent.com/40672950/77836861-afd06980-7138-11ea-9b07-5565a280a13d.png)
**CodeForce:** https://codeforces.com/contest/1297/problem/B

---

## Solução 🇧🇷

Vamos provar a próxima proposição: se a resposta não for igual a `-1 ', existe tal resposta _x_ que
> | _x − l_ | ≤ 1 ou | _x − r_ | ≤ 1 para cerca de 1 ≤ _i_ ≤ _n_.

Vamos ter a resposta _x_ e _x ≠ l_ e _x ≠ r_. Então vamos mover _x_ para a esquerda, um por um, até cumprirmos a condição acima - isso certamente acontecerá, pois existe pelo menos um _l <x_.

Podemos usar a proposição acima de tal maneira que existem apenas ** O (n) ** candidatos a uma resposta para verificar:
> _l − 1, l, l + 1, r − 1, r_ e _r + 1_ para todos _i_.

E para cada candidato, apenas calculamos o número de segmentos em que ele se encontra.

---

## Solution 🇬🇧

Let's prove the next proposition: if the answer is not equal to `−1` then exists such answer _x_ that either
> |_x−l_| ≤ 1 or |_x−r_| ≤ 1 for some 1 ≤ _i_ ≤ _n_.

Let we have the answer _x_ and _x ≠ l_ and _x ≠ r_. Then let's move _x_ to the left one by one until we fulfill the condition above — it will surely happens since there is at least one _l < x_.

We can use the proposition above in such way there are only **O(n)** candidates for an answer to check:
> _l−1, l, l+1, r−1, r_ and _r+1_ for all _i_.

And for each candidate, we just calculate the number of segments it is in.

The total complexity is **O( ∑ n2 )**.
