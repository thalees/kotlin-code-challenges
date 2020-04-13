# Problem Name

![image](https://user-images.githubusercontent.com/40672950/77836861-afd06980-7138-11ea-9b07-5565a280a13d.png)
**CodeForce:** https://codeforces.com/contest/1297/problem/E

---

## Solução 🇧🇷

Existem muitas soluções construtivas para esse problema. Vamos descrever um deles - uma pesquisa de largura pela primeira vez (**bfs**) ligeiramente modificada.

Vamos espalhar nosso subconjunto escolhido de qualquer vértice fixo (vértice 1, por simplicidade) como o **bfs** faz. Suponha que estejamos "em pé" no vértice _v ≠ 1_ e tenha arestas _(v, to1), (v, to2), ..., (v, tok)_ com vértices _toi_ que ainda não foram escolhidos.

Podemos ter certeza de que _v_ é uma folha no subconjunto atualmente escolhido, mas o que acontecerá se tentarmos adicionar _toi_ no subconjunto escolhido? Se adicionarmos _to1_, _v_ deixa de ser uma folha, mas _to1_ se torna, portanto, o número total de folhas não diminui. Se adicionarmos _to2_ depois disso, então _to2_ também se tornará uma folha - o número total de folhas é aumentado em **1**.

O vértice inicial 1 tem alguns casos extras, mas, em geral, podemos ver que o número total de folhas permanece o mesmo ou aumenta em 1 a cada etapa - para que possamos obter qualquer número de folhas de 1 ao máximo possível - e não é difícil provar que o número máximo possível de folhas tem a árvore inteira (e é um estado final de **bfs**).

Como resultado, todas as nossas modificações no algoritmo **bfs** padrão carregam o número atual de folhas e quebram quando ele se torna igual a **k**.

---

## Solution 🇬🇧

There are many constructive solutions to this problem. Let's describe one of them — a slightly modified breadth-first search (**bfs**).

Let's spread our chosen subset from any fixed vertex (vertex 1, for simplicity) as **bfs** does. Suppose we are "standing" in vertex v≠1 and have edges _(v,to1),(v,to2),...,(v,tok)_ with vertices _toi_ which aren't chosen yet.

We can be sure that _v_ is a leaf in the currently chosen subset, but what will happen if we'd try to add _toi_ in the chosen subset? If we add _to1_, then _v_ stops being a leaf but _to1_ becomes, so the total number of leaves doesn't decrease. If we'd add _to2_ after that then _to2_ also becomes a leaf — the total number of leaves is increased by 1.

The starting vertex 1 has some extra cases, but, in general, we can see that the total number of leaves stays the same or increases by 1 at each step — so we can get any number of leaves from 1 to maximum possible — and it's not hard to prove that the maximum possible number of leaves has the whole tree (and it's a finish state of **bfs**).

As a result, all our modifications of standard **bfs** algorithm are carrying the current number of leaves and breaking when it becomes equal to **k**.
