Data Criada: 26/05/2026 às 18:37
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

> [!obs]
> A lógica das matrizes em TL é a mesma da produto interno na forma usual (matricial)? Ou seja, quando fazemos TL sem ser com matrizes, não importa qual base estamos lidando, pois estamos lidando com suas entradas. Porém, quando fazemos TL com matrizes, passamos a lidar com coordenadas...


Sejam
$$
\begin{gather}
T: \mathbb{V} \rightarrow \mathbb{W} \\ \\
\mathcal{B_{\mathbb{V}}} = \{v_{1},v_{2},\dots,v_{m}\} \; \text{ e } \; \mathcal{B_{\mathbb{W}}} = \{w_{1},w_{2},\dots,w_{n}\}
\end{gather}

$$



**Como funciona essa passagem de $\mathbb{V} \rightarrow \mathbb{W}$?** Bom, essa passagem a princípio mapeia as entradas de um elemento de $\mathbb{V}$ para um elemento de $\mathbb{W}$, ou seja, ele transforma um elementos de um conjunto em outro elemento de outro conjunto por uma lei de formação arbitrária. A princípio, é difícil perceber como podemos juntá-los ou melhor, trabalhar com eles de forma mais padronizada...



**Por que usamos bases?** Porque assim garantimos a existência e a unicidade da nossa transformação linear. Além disso, a base é o que define a TL em todos os elementos do domínio (condição básica de uma função). 

Todas as Transformações Lineares podem ser descritas por uma matriz transformação, cujas entradas são
$$
A = \begin{bmatrix}\\
\left[T(v_{1})\right]_{\mathcal{B_{\mathbb{W}}}} & [T(v_{2})]_{\mathcal{B_{\mathbb{W}}}} & \dots & [T(v_{n})]_{\mathcal{B_{\mathbb{W}}}} \\ \\

\end{bmatrix}
$$
Sendo que cada $[T(v_{i})]_{\mathcal{B_{\mathbb{W}}}} \; \; \forall i \in \{1,\dots,n\}$ representa as coordenadas de $v_{i}$ na base $\mathcal{B_{\mathbb{W}}}$, isto é, certo elemento $v_{i} \in \mathbb{V}$ tem imagem $T(v_{i})$ dada por
$$
T(v_{i}) = \sum_{i=1}^{n} \alpha_{i}w_{i}
$$
Então a respectiva coluna de $[T(v_{i})]_{\mathcal{B_{\mathbb{W}}}}$ será dada por
$$
\begin{bmatrix}
\alpha_{1}  \\
\alpha_{2} \\
\dots \\
\alpha_{n}
\end{bmatrix}
$$
Uma vez de posse da matriz transformação $A$, podemos realizar a TL pela expressão
$$
\underbrace{A}_{n \times m} \; \underbrace{[v]_{\mathcal{B}_{\mathbb{V}}}}_{m \times 1} = \underbrace{[T(v)]_{\mathcal{B}_{\mathbb{W}}}}_{n \times 1}
$$
sendo $w \in \mathbb{W}$. Perceba como a transformação já troca também a base, i.e., ela nos retorna a imagem já na base do contradomínio. Vamos ver jajá uma passo a passo que deixa isso mais claro.



**Podemos usar conjuntos que não sejam bases na nossa TL?** 
Até podemos, só que nós perdemos a garantia da existência e da unicidade, isto é, pode ser que (i) não haja nenhuma TL que cumpra as transposições que definimos ou pode ser que (ii) hajam infinitas TL que o façam. Veja um exemplo de casa caso:
* (i) $T: \mathbb{R}^2 \to \mathbb{R}^2$ com as seguintes regras:
$$
\begin{gather}
T(1, 1) = (2, 3) \\
T(2, 2) = (5, 5)
\end{gather}

$$
* (ii) $T: \mathbb{R}^2 \to \mathbb{R}^2$:
$$
T(1, 1) = (2, 3)
$$
O primeiro caso (temos um conjunto LD, logo não é base) quebra a linearidade da TL, pelo que nenhuma o satisfaz. Já na segunda, não temos informação suficiente, pelo que existem infinitas.



**Afinal, por que é interessante trabalharmos com as coordenadas em vez das entradas?** Bom, nós temos infinitos EV e muitos deles são estranhos. Se quisermos manipulá-los de forma algébrica, nós precisamos arrumar um jeito de transpor os elementos de quaisquer EV para algo mais simples e que dê para representá-los por uma matriz, conforme vimos acima.

Opa, mas já temos isso! São justamente as coordenadas do elemento em determinada base. Assim, conseguimos fazer um isomorfismo de quaisquer EV de dimensão $n$ para o espaço das matrizes $\mathbb{M}_{n\times 1}$, o qual nós fazemos um abuso de notação e representamos por $\mathbb{R}^{n}$.



> [!obs] Relação com produto interno.
> No produto interno, nós tínhamos infinitas formas de definí-lo. Mas havia uma única, o produto interno usual, que nos garantia a existência para qualquer EV, isto é, ele sempre funcionava em qualquer EV.
> 
> Além disso, ele nos possibilitava, diferente de outras definições de produto interno, representá-lo na forma matricial com as coordenadas em relação à base tomada.
> 
> Aqui no contexto de Transformações Lineares, qualquer TL pode ser escrita na forma matricial. Quando isso acontece, nós estamos tomando as coordenadas dos vetores em alguma base. Isso acontece sutilmente, principalmente quando estamos pegando as entradas da matriz e passando direto para a forma matricial: nesse caso, estamos na verdade tomando as coordenadas na base canônica. Veja o exemplo abaixo:
> 
> $
> \begin{gather}
> T: \mathbb{R}^{2} \rightarrow \mathbb{R}^{2} \\
> (x,y) \mapsto (2x-4,3x+2y)
> \end{gather}
> $
> Aqui, ao denotarmos essa TL por uma matriz, teremos
> $
> A = \begin{bmatrix}
> 2  & -1 \\
> 3 & 2
> \end{bmatrix}
> $
> Pode não parecer, mas cada coluna dessas são as coordenadas (não mais as entradas $x,y$) em relação à base canônica nesse caso $\mathcal{C}=\{{e_{1},e_{2}}\}$.
> 
> **Resumindo:** nesse contexto de matrizes, nós sempre estamos trabalhando com as coordenadas em relação à alguma base, por isso a importância de sinalizá-la entre parênteses.
> 



**A matriz mudança de base tem alguma relação com isso?** Tem e muita. Voltemos na TL que leva $\mathbb{V} \rightarrow \mathbb{W}$ cujas bases são $B_{\mathbb{V}}$ e $B_{\mathbb{W}}$. Podemos pensar na matriz transformação que define uma TL genérica como sendo um cadeia de $3$ passos:
* (i) Mudar a base de $[v]_{\mathcal{B}_{\mathbb{V}}} \in \mathbb{V}$ de $\mathcal{B}_{\mathbb{V}}$ para $\mathcal{B}_{\mathbb{V}}$.
* (ii) Fazer a Transformação Linear $T: [v]_{\mathcal{C}} \mapsto [T(v)]_{\mathcal{C}}  \in \mathbb{V}$ (definida na base canônica).
* (iii) Mudar a base de $[T(v)]_{\mathcal{C}} \in \mathbb{W}$ de $\mathcal{C}$ para $\mathcal{B}_{\mathbb{W}}$.
Portanto, pensando no exemplo acima, onde lidávamos com as coordenadas na base canônica, podemos simular uma transformação genérica tal qual definimos no início dessa sessão:
$$
[T(v)]_{\mathcal{B}_{\mathbb{W}}} = \underbrace{[T(v)]_{\mathcal{\mathcal{C}} \rightarrow \mathcal{\mathcal{B}_{\mathbb{W}}}}}_{(iii)} \; \underbrace{A}_{(ii)} \;  \underbrace{[v]_{\mathcal{B}_{\mathbb{V}} \rightarrow \mathcal{C}}}_{(i)}
$$
Toda processo de mudança de base é uma Transformação Linear.