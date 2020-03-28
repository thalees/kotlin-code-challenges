# Problem Name

![alt text]("Link")
**CodeForce:** https://codeforces.com/contest/1297/problem/D

---

## Solução 🇧🇷

Primeiramente, vamos reordenar o array _a_ de modo que `a ≥ a + 1`. Então o máximo entre todos `a + d` é apenas um valor `a1 + d1`.

No primeiro passo, vejamos qual é o bônus total máximo que podemos distribuir se `d1 = 0`, então o `a1 + d1` é o mínimo possível. Podemos encontrar a próxima fórmula: `di = a1 - (i − 1) - ai` e o bônus máximo possível será igual a `∑ a1 - (i - 1) - a`.

Se _k_ não exceder o bônus máximo que podemos distribuir se `d1 = 0`, então a resposta ideal já foi encontrada e podemos distribuir o bônus _k_: dar ao primeiro empregado 0, ao segundo `a1 - 1 - a2` se pudermos (ou tudo o que tivermos se não pudermos) e assim por diante.

Caso contrário, precisamos aumentar _d1_. Mas aumentar _d1_ em 1 leva a aumentar o bônus máximo em _n_. Então, vamos definir
> rem = k - ∑ a1 - (i - 1) - ai

E podemos ver que tudo o que precisamos fazer é dar aos funcionários _rem_ **mod** _n_ adicionais `rem / n + 1` adicionais (ou `d = d + rem / n + 1`) e outros empregados `rem / n` (ou `d = d + rem / n`).

---

## Solution 🇬🇧

At first, let's reorder array _a_ in such way that `a ≥ a + 1`. Then the maximum among all `a + d` is just a value `a1 + d1`.

In the first step, let's look at what is the maximum total bonus we can distribute if `d1 = 0` (so the `a1 + d1` is the minimum possible). We can find the next formula: `di = a1 − (i−1) − ai` and the maximum possible bonus will be equal to `∑ a1 − ( i − 1 ) − a`.

If _k_ doesn't exceed the maximal bonus we can distribute if `d1 = 0` then the optimal answer is already found and we can distribute bonus _k_: give to the first employe 0, to the second `a1 − 1 − a2` if we can (or all we have if we can't) and so on.

Otherwise, we need to increase _d1_. But increasing _d1_ by 1 leads to increasing the maximal bonus by _n_. So, let's define
> rem = k − ∑ a1 − ( i − 1 ) − ai

And we can see that all we need to do is just give first _rem_ **mod** _n_ employees additional `rem/n + 1` (or `d = d + rem/n + 1`) and other employes `rem/n` (or `d = d + rem/n`).
