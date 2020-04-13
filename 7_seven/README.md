# Problem Name

![image](https://user-images.githubusercontent.com/40672950/77836861-afd06980-7138-11ea-9b07-5565a280a13d.png)
**CodeForce:** https://codeforces.com/contest/1297/problem/G

---

## Solução 🇧🇷

Observe que, como cada divisor de m deve ter um dígito menor que **10**, todos os divisores primos de _m_ devem ser menores que **10**, ou seja, podemos representar _m_ como _m = 2 ^ f1 x 3 ^ f2 x 5 ^ f3 x 7 ^ f4_. Caso contrário, a resposta é **-1**.

Agora, vamos escrever a programação dinâmica _dp_ com o estado _(f1, f2, f3, f4, len)_ que é igual ao número de _m_ números de comprimento _len_ e _m = 2 ^ f1 x 3 ^ f2 x 5 ^ f3 x 7 ^ f4_. As transições são bem diretas: vamos escolher qual é o último dígito _d_ ou verificar todos os últimos dígitos possíveis _d ∈ [** 1,9 **]_ recalcular a matriz _f_ e perguntar o valor do estado _(f′1, f′2 , f′3, f′4, len − 1)_.

O truque é que não visitaríamos tantos estados diferentes, portanto basta memorizar todos eles por meio de hash e um map.

A última pergunta é como encontrar _k_-é o menor em ordem lexicográfica. É um algoritmo bastante padrão. Em primeiro lugar, vamos encontrar o comprimento da resposta. Deve ser igual ao mínimo _len_, de modo que o número total de _m_-números de comprimento não mais que _len_ seja pelo menos _k_. Então vamos construir a resposta a partir do prefixo que decide para cada posição, qual dígito deve estar aqui. Isso pode ser feito usando o _dp_ para calcular um número de _m′_- números que possui um prefixo fixo.

---

## Solution 🇬🇧

Note, that since each divisor of _m_ should be a digit less than **10** then all prime divisors of m should be less than **10**, i.e. we can represent _m_ as _m= 2^f1 x 3^f2 x 5^f3 x 7^f4_. Otherwise, the answer is **−1**.

Now, let's just write dynamic programming _dp_ with state _(f1,f2,f3,f4,len)_ which is equal to the number of _m_-numbers of length len and _m = 2^f1 x 3^f2 x 5^f3 x 7^f4_. The transisions are quite straightforward: let's choose what the last digit _d_ is or let's check all posible last digit _d ∈ [**1,9**]_ recalculate array _f_ and ask value of state _(f′1,f′2,f′3,f′4,len−1)_ .

The trick is that we'd visit not so many different states, so it's enough just to memorize all of them by hashing and map.

The last question is how to find _k_-th smallest in lexicographical order. It's quite a standard algorithm. At first, let find the length of the answer. It should be equal to the minimum _len_ such that the total number of _m_-numbers of length no more than _len_ is at least _k_. Then let's build the answer from the prefix deciding for each position, what digit should be here. It can be done using the _dp_ to calculate a number of _m′_-numbers which has a fixed prefix.
