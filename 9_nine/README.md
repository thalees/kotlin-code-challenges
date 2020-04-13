# Problem Name

![image](https://user-images.githubusercontent.com/40672950/77836861-afd06980-7138-11ea-9b07-5565a280a13d.png)
**CodeForce:** https://codeforces.com/contest/1297/problem/I

---

## Solução 🇧🇷

Se armazenarmos, para cada altura, um conjunto ordenado de todos os blocos atualmente existentes, se soubermos a altura _**maxH**_ para começar, podemos vaporizar os blocos com eficiência suficiente ou decidir que o bloco atual parou de cair.

Podemos consultar o conjunto para esse nível para verificar se a queda foi interrompida (ou seja, se o bloco descartado entrar em contato com um bloco que não cobre). Nesse caso, pare a vaporização e lembre-se da altura final. Caso contrário, use o aparelho para determinar quais blocos devem ser vaporizados antes de repetir a gota.

A questão é: como determinar a altura inicial _**maxH**_? Se os blocos não fossem vaporizados, poderíamos usar uma Árvore de segmentos padrão com "valor definido no segmento" e "obter o máximo do segmento" para definir um bloco em alguma altura e encontrar a altura máxima dos blocos em algum segmento .

De fato, podemos usá-lo! É por causa da propriedade que o bloco vaporiza apenas os blocos que cobre, portanto, a operação "definir novo bloco" no ST substituirá todos os blocos vaporizados pelo atual e não precisamos pensar em métodos para apagar manualmente os blocos do ST.

A complexidade resultante é _**O(nlog (n))**_.

---

## Solution 🇬🇧

If we store, for each height, an ordered set of all blocks currently there then if we know, the height _**maxH**_ to start from, we can efficiently enough vaporize blocks or decide that the current block has stopped falling.

We can query the set for that level to check if the fall is stopped (i.e. if the dropped block comes in contact with a block that it does not cover). If so, stop the vaporizing and remember the final height. If not, use the set to determine which blocks to vaporize before repeating the drop.

The question is: how to determine starting height _**maxH**_? If blocks wouldn't be vaporized then we could use a standard Segment Tree with "set value on the segment" and "get the maximum on the segment" to set a block on some height and to find the maximum height of blocks on some segment.

In fact, we can use it! It's because of the property that the block vaporizes only blocks it covers, so "setting new block" operation in ST will replace all vaporized blocks with the current one and we don't need to think about methods to erase blocks from ST manually.

The resulting complexity is _**O(nlog(n))**_.
