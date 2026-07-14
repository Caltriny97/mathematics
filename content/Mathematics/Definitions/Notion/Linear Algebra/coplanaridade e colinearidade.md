Data Criada: 03/04/2026 às 23:44
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

> [!definicao] Definição.
> Dois ou mais vetores são ditos coplanares se existe algum plano que seja paralelo aos segmentos de retas orientados que representam tais vetores.

**Cuidado**: dois vetores coplanares não determinam um único [[Planos|plano]]. Para tanto, é necessário conhecer pelo menos mais um ponto do plano.

> [!obs] Obs.
> * Dois vetores sempre são coplanares (lembre que eles não têm posição fixa).
> * $A, B$ e $C$ colineares $\iff$ os vetores $u$ e $v$ formados por eles são paralelos. Ver item (ii) abaixo.
> *  $A, B, C$ e $D$ coplanares $\iff$ os vetores $u,v$ e $w$ formados por eles são coplanares. ver item (iii) abaixo.
>   
> Não confundir coplanaridade, colinearidade e paralelismo. Lembre também que vetores não tem posição fixa assim como as retas.


**Resumindo.**
- (i) $u / / v \Leftrightarrow$ um vetor é múltiplo escalar do outro ( $v=\alpha . u$ ou $u=\alpha . v$ para algum $\alpha \in \mathbb{R}$ )
- (ii) $A, B$ e $C$ colineares $\Leftrightarrow$ $u / / v \Leftrightarrow\|u \times v\|=0 \Leftrightarrow u \times v=\overline{0}$
- (iii) $A, B, C$ e $D$ coplanares $\Leftrightarrow$ $u, v$ e $w$ coplanares $\Leftrightarrow|[u, v, w]|=0 \Leftrightarrow[u, v, w]=0$
- (iv) $u / / v$ ou $u, v$ e $w$ coplanares ⇔ se **um** (ver comentário) dos vetores pode ser escrito como combinação linear dos demais.


> [!obs] Obs.
> Em (iv), pode ser que tenhamos
> ![[Pasted image 20260328230821.jpg|center|200]]
> Nessa caso, conseguimos escrever $u$ como combinação linear $\alpha w + 0v$, mas **não** conseguimos escrever $v$ como combinação linear de $u$ e $w$, porque esses estão na mesma direção. Por isso escrevemos em (iv): "se um dos vetores pode ser escrito..." e não "qualquer um dos vetores".

> [!ps]- Ps.
> **PS.** Combinação Linear: é escrever um vetor utilizando as duas propriedades básicas de um Espaço Vetorial: soma e produto por escalar. Ex.: $u=\alpha w+\beta v$ é combinação linear de $w$ e $v$.
>  ![[Pasted image 20260326205335.png|center|400]]


