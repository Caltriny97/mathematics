Data Criada: 29/05/2026 às 23:46
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

> [!definicao]
> Seja $T: \mathbb{V} \rightarrow \mathbb{W}$ uma transformação linear.
> * i) O **Núcleo** de $T$ é o conjunto $N(T)=\{v \in \mathbb{V} \mid T(v)=\overline{0}\}$.
> * ii) A **Imagem** de $T$ é o conjunto $\operatorname{Im}(T)=\{w \in \mathbb{W} \mid w=T(v)$ para algum $v \in V\}$.

> [!obs]
> O núcleo da transformação é um subconjunto dos elementos do **domínio** que é levado no núcleo.
> 
> Tem como o núcleo ser vazio? Não, porque a TL leva o vetor nulo do domínio no nulo do contradomínio. Então, em particular, o nulo está sempre no núcleo.

> [!exemplo]-
> $
> \begin{aligned}
> &\text { Ex.) } T: \mathbb{R}^n \rightarrow \mathbb{R}^n \text { dada por } T(v)=\operatorname{proju}_u v \text {. }\\
> &\begin{aligned}
> & \bullet N(T)=\left\{z \in \mathbb{R}^n \mid z \perp u\right\} \\
> & \bullet \operatorname{Im}(T)=\{\lambda u \mid \lambda \in \mathbb{R}\}
> \end{aligned}
> \end{aligned}
> $
> Esse ex é interessante, porque mostra essa relação entre núcleo e imagem, que juntos compõe a dimensão do domínio. Mas veja que os elementos de \mathbb{V} $\mathbb{V}$ em si não têm relação direta com o núcleo ou a imagem. O ponto é, essa relação é uma "coincidência".


# Propriedades 

> [!teorema]
> Seja $T: \mathbb{V} \rightarrow \mathbb{W}$ uma transformação linear e $\mathcal{B}=\left\{v_1, \ldots, v_n\right\}$ base de $\mathbb{V}$.
> * i) $\overline{0}_{\mathbb{V}} \in N(T)$ e $\overline{0}_{\mathbb{W}} \in \operatorname{Im}(T)$.
> * ii) $\operatorname{Im}(T)=\operatorname{span}\left\{T\left(v_1\right), \ldots, T\left(v_n\right)\right\}$.
> * iii) $\operatorname{Im}(T)$ é subespaço vetorial de $\mathbb{W}$.
> * iv) $N(T)$ é subespaço vetorial de $\mathbb{V}$.

O mais interessante aqui é a propriedade (ii), que nos permite conseguir a **imagem** a partir apenas da **base do domínio** (pode ser qualquer uma). 
* Assim, não precisamos ficar tentando caracterizar quem é a imagem, através da lei geral da TL.
* Aplicando essa propriedade (ii), nós conseguimos um gerador para a imagem. Se esse gerador for LI, nós conseguimos uma base para a imagem.
* Como consequência disso, a imagem é um subespaço vetorial, porque todo span é um SV.
Caracterizar o núcleo é mais simples: basta resolvermos o sistema linear homogêneo.

> [!exemplo]- Bases espertas...
> Podemos pegar qualquer base, mas a depender da situação, algumas podem ser mais espertas do que outras...
> 
> Ex.: 
> $
> T: \mathbb{R}^3 \rightarrow \mathbb{R}^3 \text { dada por } T(v)=\operatorname{proju}_{e_2} v
> $
> Tomando a base canônica, sai direto que
> $
> \text{Im}(T)=\operatorname{span}\{\bar{0}, e_2, \bar{0}\}
> $

> [!exemplo]- Novas soluções?
> $
> \begin{aligned}
> &\text { Ex. } T: \mathbb{R}^4 \rightarrow \mathbb{R}^2 \text { dada por } T(x, y, z, w)=(2 x, y+z) \text {. Encontrar } N(T) \text { e } \operatorname{Im}(T) \text {. }\\
> &\begin{aligned}
> \bullet (x, y, z, w) \in N(T) & \Leftrightarrow T(x, y, z, w)=(0,0) \\
> & \Leftrightarrow(2 x, y+z)=(0,0) \\
> & \Leftrightarrow\left\{\begin{array}{l}
> 2 x=0 \\
> y+z=0
> \end{array}\right. \\
> & \Leftrightarrow x=0 \text { e } y=-z \\
> & \Leftrightarrow(x, y, z, w)=(0,-z, z, w)=z(0,-1,1,0)+w(0,0,0,1) \\
> & \therefore N(T)=\operatorname{span}\{(0,-1,1,0),(0,0,0,1)\} \\
> \bullet \operatorname{Im}(T)= & \operatorname{span}\{T(1,0,0,0), T(0,1,0,0), T(0,0,1,0), T(0,0,0,1)\} \\
> = & \operatorname{span}\{(2,0),(0,1),(0,1),(0,0)\} \\
> = & \operatorname{span}\{(2,0),(0,1)\}=\mathbb{R}^2
> \end{aligned}
> \end{aligned}
> $
> Sabemos $(x,y,z) = \bar{0} \implies T((x,y,z)) = T(\bar{0})$. Se é só um caminho de ida, então soluções novas podem aparecer no meio do caminho. Então porque as condições $x=0$ e $y=-z$ devem ser impostas logo no "início", i.e., em $(x,y,z,w)$? O ponto é que:
> $
> T((x,y,z)) = T(\bar{0}) \iff (0,-z,z,w) = \bar{0}
> $
> Outra **obs** é que ela está pegando a base canônica, mas poderia ser uma **base qualquer** de $\mathbb{R^4}$.


$$
\begin{aligned}
T: \mathbb{M}_{n \times 1} & \rightarrow \mathbb{M}_{m \times 1} \\
X & \mapsto  T(X) = A X
\end{aligned}
$$
Acima, estamos lidando diretamente com as entradas das matrizes (poderia ser quaisquer outros EV). Poderíamos também representá-las em termos das suas **coordenadas** em relação a alguma base $\mathcal{C}$. Para isso, usamos fazemos um abuso de notação, representando-o através do seu **isomorfo** em $\mathbb{R}^{k}$.
$$
\begin{aligned}
T: \mathbb{R}^n & \rightarrow \mathbb{R}^m \\
X & \mapsto  [T(X)]_{\mathcal{C}} = A[X]_{\mathcal{C}}
\end{aligned}
$$
Diferentemente do que acontecia no produto interno, não podemos simplesmente trocar a base de $\mathcal{C}$ para uma $\mathcal{B}$ por ex, porque a matriz transformação $A$ depende diretamente da base escolhida, portanto ela deveria mudar também. 

> [!container] Núcleo
> $
> \begin{gather}
> X \in N(T) \Leftrightarrow T(X)=\overline{0} \Leftrightarrow A X=\overline{0} . \\ \\
> N(T)=\text { Conjunto solução do SLH definido por } A \text {. }
> \end{gather}
> 
> $
> Por enquanto, achar $N(T)$ por meio do conjunto solução do SLH só está provado para TL definidas por matrizes. Porém, vamos ver já que **toda TL pode ser definida por uma matriz.** Até agora, só provamos a volta.

Aqui, estamos considerando $X$ na base canônica. Ver [[Matriz de uma Transformação Linear]] para mais detalhes dessa discussão.

> [!container] Imagem.
> $
> \begin{gathered}
> \operatorname{Im}(T)=\operatorname{span}\left\{A\left[\begin{array}{l}
> 1 \\
> 0 \\
> \vdots \\
> 0
> \end{array}\right], A\left[\begin{array}{l}
> 0 \\
> 1 \\
> \vdots \\
> 0
> \end{array}\right], \ldots, A\left[\begin{array}{l}
> 0 \\
> 0 \\
> \vdots \\
> 1
> \end{array}\right]\right\}=\operatorname{span}\left\{\left[\begin{array}{c}
> a_{11} \\
> a_{21} \\
> \vdots \\
> a_{m 1}
> \end{array}\right],\left[\begin{array}{c}
> a_{12} \\
> a_{22} \\
> \vdots \\
> a_{m 2}
> \end{array}\right], \ldots,\left[\begin{array}{c}
> a_{1 n} \\
> a_{2 n} \\
> \vdots \\
> a_{m n}
> \end{array}\right]\right\} \\ \\
> \operatorname{Im}(T)=\text { Espaço coluna de } A .
> \end{gathered}
> $
> 
> Estamos usando nosso resultado de que $\operatorname{Im}(T)=\operatorname{span}\left\{T\left(v_1\right), \ldots, T\left(v_n\right)\right\}$, tomando uma base $\mathcal{B}= \{v_{1},\dots,v_{n}\}$. Acima, estamos tomando a base canônica.
> 
> O ponto é que, ao fazer as transformações $T(e_{1}), \dots, T(e_{n})$, estamos fazendo na verdade $Ae_{1},\dots ,Ae_{n}$, oque resulta exatamente no span das colunas de $A$.


# Posto e Nulidade

> [!definicao]
> Seja $T: \mathbb{V} \rightarrow \mathbb{W}$ uma transformação linear.
> * i) A dimensão de $\operatorname{Im}(T)$ é chamada de **posto** de $T$.
> * ii) A dimensão de $N(T)$ é chamada de **nulidade** de $T$.

Nós tínhamos visto que posto é a dimensão do espaço coluna. Mas isso é a mesma coisa que a dimensão da imagem, por isso estamos aproveitando-o.


> [!teorema]
> Para toda transformação linear $T: \mathbb{V} \rightarrow \mathbb{W}$ tem-se
> $
> \operatorname{dim}(\mathbb{V})=\operatorname{dim} N(T)+\operatorname{dim} \operatorname{Im}(T) .
> $

Ver demonstração na minha nota de aula 16 (tem uma obs no final sobre soluções de SL, quando um implica outro).

> [!obs]
> $
> \begin{aligned}
> T: \mathbb{R}^n & \rightarrow \mathbb{R}^m \\
> X & \mapsto A X
> \end{aligned}
> $
> 
> i) Posto $=\operatorname{dim}(\operatorname{Im}(T))=$ dimensão espaço coluna de $A=$ número de pivôs de $A$.
> 
> ii) Nulidade $=\operatorname{dim}(N(T))=\operatorname{dim}(\mathbb{V})-$ posto $=n^{\circ}$ de incógnitas $-n^{\circ}$ de pivôs de $A=n^{\circ}$ de variáveis livres.