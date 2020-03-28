# Problem Name

![alt text]("Link")
**CodeForce:** https://codeforces.com/contest/1297/problem/C

---

## Solução 🇧🇷

Pode-se provar que existem apenas duas configurações que precisamos considerar:

- A primeira que o subconjunto com a soma máxima, porém sem o menor elemento positivo. Isso é possível se houver pelo menos dois elementos positivos no array _a_.
- A segunda que o subconjunto com a soma máxima, porém com um elemento negativo extra (obviamente, deve ser aquele com o menor valor absoluto). Isso é possível se houver pelo menos um elemento negativo no array _a_.

Podemos verificar as duas configurações separadamente ou simultaneamente em tempo linear e escolher a melhor.

_P.S .: Não é difícil provar que a configuração não deve ter mais de um elemento positivo (uma vez que, por outro lado, podemos retornar outros elementos e melhorar a resposta) em comparação ao subconjunto com soma máxima. Da mesma maneira, a configuração **não deve ter mais que um elemento negativo extra**._

---

## Solution 🇬🇧

It can be proven that there are only two configurations that we need to consider:

- The first that the subset with the maximum sum, but without the least positive element. This is possible if there are at least two positive elements in the _a_ array.
- The second that the subset with the maximum sum, but with an extra negative element (obviously, must be the one with the lowest absolute value). This is possible if there is at least one negative element in the _a_ array.

We can check both configurations separately or simultaneously in linear time and choose the best one.

_P.S.: It's not hard to prove that the configuration should have no more than one positive element being absent (since, in the other way, we can return other elements and make the answer better) comparing to the subset with maximal sum. In the same manner, the configuration should have no more than one extra negative element._
