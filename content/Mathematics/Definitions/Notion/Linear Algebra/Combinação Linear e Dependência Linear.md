Data Criada: 20/04/2026 às 22:09
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

Ao longo desta nota, o conjunto denotado por $\mathbb{V}$ sempre será considerado como sendo um espaço vetorial.

# Combinação Linear

$$
\begin{gather}
A X=\left[\begin{array}{cccc}
a_{11} & a_{12} & \ldots & a_{1 n} \\
a_{21} & a_{22} & \ldots & a_{2 n} \\
\vdots & & & \vdots \\
a_{m 1} & a_{m 2} & \ldots & a_{m n}
\end{array}\right]\left[\begin{array}{c}
x_1 \\
x_2 \\
\vdots \\
x_n
\end{array}\right]=x_1\left[\begin{array}{c}
a_{11} \\
a_{21} \\
\vdots \\
a_{m 1}
\end{array}\right]+x_2\left[\begin{array}{c}
a_{12} \\
a_{22} \\
\vdots \\
a_{m 2}
\end{array}\right]+\cdots+x_n\left[\begin{array}{c}
a_{1 n} \\
a_{2 n} \\
\vdots \\
a_{m n}
\end{array}\right] \\
 \\ \\
 
\text{$A X=B$ tem solução se, e somente se, $B$ pode ser escrito como} \\
\text{\textbf{soma de múltiplos escalares} das colunas de $A$.}
\end{gather}
$$

Nós sabemos que o conjunto de matrizes $\mathbb{M}_{m \times 1}$ nas operações usuais é um EV. Portanto, o que temos acima é uma **combinação linear** dos vetores desse EV, que representam as colunas de $A$.

Mas por que estamos interessados em enunciar desta forma?

> [!definicao]
> Um vetor $w \in \mathbb{V}$ é dito **combinação linear** dos vetores $v_1, \ldots, v_k \in \mathbb{V}$ se existem escalares $\alpha_1, \ldots, \alpha_k \in \mathbb{R}$ tais que satisfazem a equação
> 
> $
> w=\alpha_1 v_1+\ldots+\alpha_k v_k .
> $
> 
> 
> Neste caso, dizemos também que o vetor $w$ é **gerado** por $v_1, \ldots, v_k$.

Reescrevendo o que enunciamos antes:
$A X=B$ tem solução se, e somente se, $B$ pode ser escrito como combinação linear das colunas de $A$ ( $B$ é gerado pelas colunas de $A$ ), onde os coeficientes da combinação linear são justamente os elementos que formam a solução do SL.


> [!relembrando]
> Em GA, o conceito de $1$ vetor ser combinação linear de outro vetor é equivalente de serem paralelos. Já para $1$ vetor ser combinação linear de outros $2$ vetores é equivalente de serem coplanares. Relembre [[coplanaridade e colinearidade]]. O que estamos fazendo aqui é generalizar esses conceitos de elementos serem gerados por outros para qualquer EV.
> 
> Ver visualização do [3blue1brown](https://youtu.be/k7RM-ot2NWY?si=cqufyX4uSWPI3T0E).

**Obs:** O vetor nulo $\overline{0}$ é gerado por quaisquer outros vetores do mesmo espaço vetorial (pela propriedade $0 \odot v = \bar{0}$ que vimos em [[Espaços Vetoriais e Subespaços Vetoriais]]):
$$
\overline{0}=0 . v_1+\ldots+0 . v_k
$$


# Espaço Gerado

> [!obs]
> Façamos a associação $\mathbb{M}_{3 \times 1} \rightarrow \mathbb{R}^{3}$ de matrizes com os vetores de GA no $\mathbb{R}^{3}$. Ver [[Notação Matricial]]. Agora, vamos pensar no sistema $A_{3 \times 2}X_{2 \times 1}=B_{3 \times 1}$. 
> 
> ![[Pasted image 20260422214007.jpg|center|400]]
> 
> Para que esse SL tenha solução, $B$ deve morar no mesmo espaço que as colunas de $A$. Se fizermos a transição $\mathbb{M}_{3 \times 1} \rightarrow \mathbb{R}^{3}$, temos que $B$ deve estar no plano dos vetores $A_{1}$ e $A_{2}$ que representam as colunas de $A$.
> 
> Aqui, perceba que nós fazemos a pergunta invertida: dado $A$, quais serão todas as possibilidades de $B$ para que $AX=B$ tenha solução. Até agora, vimos analisando $A$. 

> [!problema]
> Qual a relação disso com conjunto solução de SL homogêneo, já que esses espaços gerados são subespaços vetoriais e passam todos pela origem (pelo que vimos nas discussões de [[MOC - Álgebra Linear]]).

> [!comentario]-
> Essa ideia de espaço gerado, de todos os vetores gerados é muito importante para entendermos aonde que estamos chegando quando fazemos algo da forma $AX$, com $X$ uma matriz coluna. Não estamos olhando para um $B$ específico, mas sim todo o conjunto que conseguimos atingir através da matriz $A$. Em outras palavras, fazendo combinações lineares das colunas de $A$, qual o conjunto que conseguimos atingir, quais são os possíveis $B$ para os quais temos solução.


> [!definicao]
> O **Espaço Gerado** pelos vetores $v_1, \ldots, v_k \in \mathbb{V}$ é o conjunto de todos as combinações lineares destes vetores.
> Notação: $\operatorname{span}\left\{v_1, \ldots, v_k\right\}$ ou $\left[v_1, \ldots, v_k\right]$

> [!exemplo]
> $
> \begin{gather}
> S = \left\{ y \in \mathbb{M}_{3 \times 1}; \; \exists \, x_{1} \text{ e } x_{2} \in \mathbb{R} \text{ tal que } \; y = x_{1} 
> \left[
> \begin{array}{cccc}
> 2  \\
> 1  \\
> 0  \\
> \end{array} 
> \right]
> + x_{2}
> \left[
> \begin{array}{cccc}
> -1  \\
> 3  \\
> 0  \\
> \end{array} 
> \right]
> \right\}  \\ \\
> 
> = \operatorname{span}\left\{ \left[
> \begin{array}{cccc}
> 2  \\
> 1  \\
> 0  \\
> \end{array} 
> \right],
> \left[
> \begin{array}{cccc}
> -1  \\
> 3  \\
> 0  \\
> \end{array} 
> \right] \right\}
> \end{gather}
> 
> $
> 
> Estamos usando matrizes colunas apenas para seguir a visualização de SL da nossa observação acima, mas essas definições valem para qualquer EV, como $\mathbb{M}_{2 \times 2}$.


> [!teorema]
> O espaço gerado por $v_1, \ldots, v_k \in \mathbb{V}$ é um subespaço vetorial de $\mathbb{V}$.

Isso explica porque chamamos esse conjunto de espaço. Ver demonstração na nota de aula 10. Para melhor compreensão desse conceito, veja também o problema 8 da lista 6.

> [!exemplo]- Espaço gerado de uma reta.
> Para uma reta de GA ser um espaço vetorial, ela deve passar pela origem (ver discussões). Sua equação vetorial é:
> $
> \begin{aligned}
> &r:X=(0,0,0) + t(2,3,4) = t(2,3,4) \\
> &r = \text{span}\{(2,3,4)\}
> \end{aligned}
> $
> Todos os elementos da reta são combinações lineares do vetor diretor, ou seja, a reta é gerada por esse vetor.
> 
> O mesmo acontece com um plano que passa pela origem.


# Espaço Linha, Espaço Coluna e Espaço Nulo

> [!definicao]
> Seja $A$ uma matriz $m \times n$.
> * a) O espaço gerado pelas colunas de $A$ é chamado de **espaço coluna** de $A$.
> * b) O espaço gerado pelas linhas de $A$ é chamado de **espaço linha** de $A$.
> * c) O espaço solução do sistema linear homogêneo $A X=\overline{0}$ é denominado **espaço nulo** de $A$.

> [!exemplo]-
> $
> \begin{gather}
> \text{Dado uma matriz} \quad A = \left[ 
> \begin{array}{cccc}
> 1 & 2 & 3\\
> 4 & 5 & 6\\
> 7 & 8 & 9\\
> 10 & 11 & 12
> \end{array}
> \right] \quad \text{segue que}\\ \\
> 
> \text{span}\{[1,2,3], [4,5,6], [7,8,9], [10,11,12]\} \subseteq \mathbb{M}_{1 \times 3}\\ \\
> 
> \text{span}\left\{
> \left[\begin{array}{cccc}
> 1 \\
> 4 \\
> 7 \\
> 10
> \end{array}
> \right], 
> \left[\begin{array}{cccc}
> 2 \\
> 5 \\
> 8 \\
> 11
> \end{array}
> \right], \\
> \left[\begin{array}{cccc}
> 3 \\
> 6 \\
> 9 \\
> 12
> \end{array}
> \right] 
> 
> \right\} \subseteq \mathbb{M}_{4 \times 1}
> \end{gather}
> $
> 
> Perceba que são subespaços de espaços vetoriais diferentes.
> 
> Já falamos sobre o espaço nulo de $A$ em [[Sistemas Lineares]] Homogêneos.

> [!corolario]-
> - O espaço linha de $A$ é igual ao espaço coluna de $A^T$.
> - O espaço linha de $A$ e o espaço coluna de $A$ são subespaços vetoriais.
>   
> $A X=B$ tem solução se, e somente se, $B$ pertence ao espaço coluna de $A$

> [!resumo]- $A X=B$ tem solução $\iff$ (...)
> $A X=B$ tem solução se, e somente se,
> - $B$ pode ser escrito como soma de múltiplos escalares das colunas de $A$.
> - $B$ pode ser escrito como combinação linear das colunas de $A$.
> - $B$ é gerado pelas colunas de $A$.
> - $B$ pertence ao espaço gerado pelas colunas de $A$.
> - $B$ pertence ao espaço coluna de $A$.


# Dependência e Independência Linear

Será que em todo EV nós conseguimos achar um **conjunto finito** de vetores que gera os infinitos vetores do EV (a única exceção é o EV formado pelo vetor nulo, que é unitário). Isso é muito interessante, pois conseguiríamos representar qualquer outro vetor por um número finito de elementos.

> [!exemplo]-
> $
> \begin{aligned}
> &S_1=\{(1,1,2),(1,0,0)\} \text { e } S_2=\{(1,1,2),(1,0,0),(2,1,2)\} \\
> & \qquad \operatorname{span}\left\{S_1\right\}=\operatorname{span}\left\{S_2\right\} \\
> & \begin{aligned}
> v \in \operatorname{span}\left\{S_1\right\} \Rightarrow v= & \alpha_1(1,1,2)+\alpha_2(1,0,0)+0 .(2,1,2) \in \operatorname{span}\left\{S_2\right\} \Rightarrow \operatorname{span}\left\{S_1\right\} \subseteq \operatorname{span}\left\{S_2\right\} \\
> v \in \operatorname{span}\left\{S_2\right\} \Rightarrow v= & \alpha_1(1,1,2)+\alpha_2(1,0,0)+\alpha_3(2,1,2) \\
> = & \alpha_1(1,1,2)+\alpha_2(1,0,0)+\alpha_3((1,1,2)+(1,0,0)) \\
> = & \left(\alpha_1+\alpha_3\right)(1,1,2)+\left(\alpha_2+\alpha_3\right)(1,0,0) \in \operatorname{span}\left\{S_1\right\} \\
> \Rightarrow & \operatorname{span}\left\{S_2\right\} \subseteq \operatorname{span}\left\{S_1\right\}
> \end{aligned}
> \end{aligned}
> $
> Perceba que $S_2 \nsubseteq S_1$. Mas pode ser que $\text{span}\{S_{2}\} \subseteq \text{span}\{S_{1}\}$. E de fato isso é verdade. Ver slides 10 para acompanhar melhor.
> 
> Nem sempre isso é possível. O que aconteceu aqui é que nós conseguimos escrever o terceiro elemento de $S_2$ como **combinação linear** dos demais, mas nem sempre é tão fácil assim...

O ponto aqui é, se nós temos $\mathbb{W} =\operatorname{span}\left\{S_1\right\}=\operatorname{span}\left\{S_2\right\}=(\dots)=\operatorname{span}\left\{S_i\right\}=(\dots)$, é sempre melhor usarmos o conjunto $S_{i}$ com menor quantidade de elementos. Para o acharmos, é preciso garantir que esse conjunto não tenha **redundância**.

De forma geral, nós queremos tirar quem é combinação linear dos demais: quem é **linearmente dependente**. 

Para saber se você pode tirar um vetor e manter o mesmo espaço, a pergunta é sempre: "O vetor que eu estou tirando pode ser reconstruído pelos que sobraram?" Essa é a forma mais intuitiva de entender o conceito de LD e LI, só que não é prático na hora de calcular. Por isso, vamos definir de modo conveniente.

> [!definicao]
> Sejam $v_1, v_2, \ldots, v_k, k \geqslant 1$, vetores de um espaço vetorial $\mathbb{V}$. $O$ conjunto $S=\left\{v_1, v_2, \ldots, v_k\right\}$ é dito **Linearmente Independente** (LI) quando a equação vetorial
> 
> $
> \alpha_1 v_1+\alpha_2 v_2+\ldots+\alpha_k v_k=\overline{0}
> $
> 
> admite somente a **solução trivial** $\left(\alpha_1=\alpha_2=\cdots=\alpha_k=0\right)$. Caso contrário, $S$ é dito **Linearmente Dependente** (LD).

> [!teorema]
> Sejam $v_1, v_2, \ldots, v_k, k \geqslant 1$, vetores de um espaço vetorial $\mathbb{V}$.
> (i) $S=\left\{v_1\right\}$ será Linearmente Dependente se, e somente se, $v_1=\overline{0}$.
> (ii) $S=\left\{v_1, v_2, \ldots, v_k\right\}, k>1$, será Linearmente Dependente se, e somente se, um destes vetores é combinação linear dos demais.

> [!demonstracao]- Demonstração (ii).
> $
> \begin{aligned}
> &\begin{aligned}
> (\Rightarrow) S & =\left\{v_1, v_2, \ldots, v_k\right\} \text { é LD } \\ \\
> & \Rightarrow \alpha_1 v_1+\alpha_2 v_2+\ldots+\alpha_k v_k=\overline{0} \text { com algum } \alpha_i \neq 0 \\ \\
> & \Rightarrow-\alpha_i v_i=\alpha_1 v_1+\alpha_2 v_2+\ldots+\alpha_{i-1} v_{i-1}+\alpha_{i+1} v_{i+1}+\ldots+\alpha_k v_k \\ \\
> & \Rightarrow v_i=\frac{\alpha_1}{-\alpha_i} v_1+\frac{\alpha_2}{-\alpha_i} v_2+\ldots+\frac{\alpha_{i-1}}{-\alpha_i} v_{i-1}+\frac{\alpha_{i+1}}{-\alpha_i} v_{i+1}+\ldots+\frac{\alpha_k}{-\alpha_i} v_k \\ \\
> (\Leftarrow) & v_i=\alpha_1 v_1+\alpha_2 v_2+\ldots+\alpha_{i-1} v_{i-1}+\alpha_{i+1} v_{i+1}+\ldots+\alpha_k v_k \\ \\
> & \Rightarrow \alpha_1 v_1+\alpha_2 v_2+\ldots+\alpha_{i-1} v_{i-1}+(-1) v_i+\alpha_{i+1} v_{i+1}+\ldots+\alpha_k v_k=\overline{0} \\
> & \Rightarrow S \text { é LD. }
> \end{aligned}
> \end{aligned}
> $

Essa definição e esse teorema torna a verificação muito mais prática do que testar os vetores um a um e ver se pode ser escrito como combinação linear dos demais.


> [!exemplo]
> $\text { Ex. } S_2=\{(1,1,2),(1,0,0),(2,1,2)\}$
> $
> \begin{aligned}
> &\begin{aligned}
> & \alpha_1(1,1,2)+\alpha_2(1,0,0)+\alpha_3(2,1,2)=(0,0,0) \\
> \end{aligned}
> \end{aligned}
> $
> Ao montar e resolver o sistema, achamos que $\alpha_1=-\alpha_3$ e $\alpha_2=-\alpha_3$, pelo que podemos escolher $\alpha_3=1$ e tomar $\alpha_1=-1$, que é diferente de zero. Assim vemos que há redundância, ou seja, o vetor que está sendo multiplicado por $\alpha_3$ é redundante aos outros dois. Veja o teorema grifado no livro do Elon e o problema 8.a da lista 7.


> [!obs]- Coplanaridade e Colinearidade.
> Seja $S=\left\{v_1, v_2, \ldots, v_k\right\} \subseteq \mathbb{R}^3$ um conjunto LD.
> - $k=1: S=\{(0,0,0)\}$
> - $k=2: S=\left\{v_1, v_2\right\} \Rightarrow v_1$ e $v_2$ são paralelos
> - $k=3: S=\left\{v_1, v_2, v_3\right\} \Rightarrow v_1, v_2$ e $v_3$ são coplanares
>   
> Esses conceitos de LI e LD são uma generalização do paralelismo para dois vetores e coplanaridade para três vetores em GA. Relembre [[coplanaridade e colinearidade]].


> [!teorema]
> Um conjunto que contém o vetor nulo sempre é linearmente dependente.
> 
> Seja $S=\left\{v_1, v_2, \ldots, v_k\right\}$ com $v_i=\overline{0}$.
> 
> $
> 0 v_1+0 v_2+\ldots+0 v_{i-1}+0 v_{i+1}+\ldots+0 v_k=\overline{0}
> $


> [!teorema]
> Sejam $S$ e $\tilde{S}$ subconjuntos finitos de um espaço vetorial $\mathbb{V}$.
> * i) Se $S$ é LD e $S \subset \tilde{S}$, então $\tilde{S}$ também é LD.
> * ii) Se $S$ é LI e $S \supset \tilde{S}$, então $\tilde{S}$ também é LI.

> [!demonstracao]- Demonstração (i)
> $
> \underbrace{\alpha_{i}v_{i}+\dots \alpha_{k}v_{k}}_{=\bar{0} \;\text{com algum $\alpha_{i} \neq 0$}}+\alpha_{k+1}+\dots+\alpha_{p}v_{p}=\bar{0}
> $
> Escolhendo $\alpha_{k+1}=\dots=a_{p}=0$, temos que existe solução não trivial, logo $S$ é LD.

> [!obs]-
> Se nós temos
> $
> S = \{\underbrace{v_{1},v_{2},v_{3}}_{LI},\underbrace{v_{4},v_{5},v_{6}}_{LI}\}
> $
> isso não implica que $S$ é LI...
> 
> Outra observação é que, quando temos um conjunto LI e adicionamos um elemento, nós só precisamos verificar se esse vetor é combinação linear dos demais. Faz sentido, pois, se ele for combinação linear dos demais, é redundante. Se não for, ele está adicionando informação nova no conjunto e o todo mantém-se LI. Agora, se adicionarmos dois, aí teríamos que fazer as combinações entre eles, daí vale mais a pena só aplicar a equação vetorial da definição.


> [!comentario]-
> Os eixos que usamos estão atrelados a elementos básicos que são geradores e têm a propriedade que estamos explorando aqui. Nós estamos generalizando o conceito dos geradores dos eixos.


# LI e LD em termos Matriciais no $R^{n}$

Seja $S=\left\{v_1, v_2, \ldots, v_k\right\} \subseteq \mathbb{R}^n$.

$$
\alpha_1 v_1+\alpha_2 v_2+\ldots+\alpha_k v_k=\overline{0} \Leftrightarrow\left[\begin{array}{llll}
v_1 & v_2 & \ldots & v_k
\end{array}\right]\left[\begin{array}{c}
\alpha_1 \\
\alpha_2 \\
\vdots \\
\alpha_k
\end{array}\right]=\left[\begin{array}{c}
0 \\
\vdots \\
0
\end{array}\right]
$$

Podemos fazer a associação $\mathbb{R}^{n} \rightarrow \mathbb{M}_{n \times 1}$ (relembre [[Notação Matricial]]). Assim, $v_{1}, v_{2},\dots,v_{k}$ podem ser representados como matrizes colunas com $n$ entradas (as coordenadas de $\mathbb{R}^{n}$). 

$$
\begin{gather}
A X=\left[\begin{array}{cccc}
a_{11} & a_{12} & \ldots & a_{1 k} \\
a_{21} & a_{22} & \ldots & a_{2 k} \\
\vdots & & & \vdots \\
a_{n 1} & a_{n 2} & \ldots & a_{n k}
\end{array}\right]\left[\begin{array}{c}
\alpha_1 \\
\alpha_2 \\
\vdots \\
\alpha_k
\end{array}\right]=\underbrace{\alpha_1\left[\begin{array}{c}
a_{11} \\
a_{21} \\
\vdots \\
a_{n 1}
\end{array}\right]+\alpha_2\left[\begin{array}{c}
a_{12} \\
a_{22} \\
\vdots \\
a_{n 2}
\end{array}\right]+\cdots+\alpha_k\left[\begin{array}{c}
a_{1 k} \\
a_{2 k} \\
\vdots \\
a_{n k}
\end{array}\right]}_{\text{É LI $\iff$ se $AX=0$ só admite solução trivial}}
\end{gather}
$$

Para o caso $n=k, \; \exists! \text{ solução} \iff \operatorname{\det}(A) \neq 0$. Relembre [[O Determinante]].

> [!teorema]
> Seja $A$ uma matriz $n \times m$.
> * (i) As colunas de $A$ são LI se, e somente se, $A X=\overline{0}$ só admite a solução trivial.
> * (ii) Se $m=n$, então as colunas de $A$ são LI se, e somente se, $\operatorname{det}(A) \neq 0$.

> [!corolario]
> Em $\mathbb{R}^n$, um conjunto com mais de $n$ vetores sempre será LD.
> 
> **Intuição**: Num Sistema Linear $AX=\bar{0}$ em que há mais incógnitas do que equações, o SL possui infinitas ou nenhuma solução. Como é homogêneo, sabemos que só pode haver infinitas, logo há solução não trivial e, portanto, o conjunto é LD.

