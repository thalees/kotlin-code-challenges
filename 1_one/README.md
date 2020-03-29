# Likes Displays

![image](https://user-images.githubusercontent.com/40672950/77836861-afd06980-7138-11ea-9b07-5565a280a13d.png)
**CodeForce:** https://codeforces.com/contest/1297/problem/A

---

## Solução 🇧🇷

Existem três variantes diferentes para exibir n:
 - Número exato,
 - Milhares
 - Milhões.

Vamos descobrir qual intervalo n deve estar para cada variante:

- Se n ∈ [0,999], devemos imprimir seu valor exato;
- Se n ∈ [1000,999499], devemos imprimi-lo como um número de milhares arredondado para o valor mais próximo;
caso contrário, devemos imprimi-lo como um número de milhões também arredondado para o valor mais próximo.

A última pergunta é:
> _Como arredondar para o número mais próximo de milhares (milhões) ?_

Existem duas maneiras de fazer isso:

Podemos evitar o uso de números com pontos flutuantes, ou seja, usar a fórmula `⌊n + 5001000⌋ (ou ⌊n + 5⋅105106⌋)`
ou podemos usar a função `roundToInt()` no valor Double.

Neste caso, usaremos a função de arredondamento.

---

## Solution 🇬🇧


There are three different variants to display n:
 - Exact number
 - Thousands
 - Millions.

Let's find out what range n should be in for each variant:

- If n∈[0,999] then we should print its exact value;
- If n∈[1000,999499] then we should print it as a number of thousands rounded to the nearest value;
otherwise we should print it as a number of millions also rounded to the nearest value.

The last question is:

> _How to round to the nearest number of thousands (millions). ?_

There are two ways to do it:

We can avoid using numbers with floating points, i.e. use formula `⌊n+5001000⌋ (or ⌊n+5⋅105106⌋)`
or we can use `roundToInt()` function on Double value.

In this case, we will use the rounding function.
