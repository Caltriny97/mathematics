Data Criada: 29/05/2026 às 23:41
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

# Introdução

Fixada uma matriz $A_{m \times n}$, seja
$$
\begin{array}{rlrl}
T: \mathbb{R}^n & \rightarrow \mathbb{R}^m & T: \mathbb{R}^n & \rightarrow \mathbb{R}^m \\
X & \mapsto T(X)=A X & X & \mapsto[T(X)]_{C^m}=A[X]_{C^n}
\end{array}
$$
No lado esquerdo, estamos fazendo um abuso de notação. Na verdade, o que estamos fazendo é o que está do lado direito: 
* As matrizes $X$ e $T(x)=AX$ estão em termos das coordenadas, por isso estão sendo representadas por um vetor em $\mathbb{R}^{n}$ e $\mathbb{R}^{m}$. Relembre [[Bases e Coordenadas]].
* Vale lembrar que isso vale para qualquer EV: de matrizes colunas, matrizes quaisquer, polinômios, etc. Todos podem ser representados em termos de uma matriz coluna dada uma base.
* Por fim, nós denotamos essa matriz coluna com as entradas das coordenadas pelo $\mathbb{R}^{n}$ de respectiva dimensão, completando a notação.



> [!teorema]
> Seja $\mathcal{C}^n$ a base canônica do $\mathbb{R}^n$ e $\mathcal{C}^m$ a base canônica do $\mathbb{R}^m$. Fixada uma matriz $A_{m \times n}$, a função
> 
> $
> \begin{aligned}
> T: \mathbb{R}^n & \rightarrow \mathbb{R}^m \\
> X & \mapsto[T(X)]_{\mathcal{C}^m}=A[X]_{\mathcal{C}^n}
> \end{aligned}
> $
> 
> é uma Transformação Linear.

Então, veja que a multiplicação por uma matriz fixada define uma TL não apenas de $\mathbb{M}_{n\times 1} \rightarrow \mathbb{M}_{m\times 1}$, mas sim de qualquer EV que admite base, uma vez que conseguimos trabalhar nas coordenadas.

Em outras palavras, dada uma matriz $A$, nós conseguimos definir uma TL para qualquer EV de dimensão finita maior ou igual que $1$ que tomemos. Vamos ver mais pra frente que a recíproca é verdadeira: toda TL pode ser descrita por uma matriz também.

No enunciado do teorema, fala-se apenas do caso de $\mathbb{R}^n \rightarrow \mathbb{R}^m$, mas isso é mais geral: podemos trocá-los por quaisquer EV de dimensões $n$ e $m$ e qualquer base de cada um dos dois.

Claro que se mudamos a base, também mudamos a TL. Mas, fixado os EV e as bases, conseguimos definir uma TL matricialmente.

> [!discussao]
> [[Transformações Lineares - conexões]]


# Matriz de uma TL

Vimo até aqui que, dada uma matriz qualquer, conseguimos definir uma TL. Agora, veremos que qualquer TL pode ser descrita por uma matriz.

Ex. Seja $T: \mathbb{R}^n \rightarrow \mathbb{R}^m$ uma transformação linear nas bases canônicas.

$$
\begin{gathered}
T(X)=T\left(x_1 e_1+x_2 e_2+\ldots+x_n e_n\right)=x_1 T\left(e_1\right)+x_2 T\left(e_2\right)+\ldots+x_n T\left(e_n\right) \\
T\left(e_1\right)=a_{11} e_1+a_{21} e_2+\ldots+a_{m 1} e_m=\left(a_{11}, a_{21}, \ldots, a_{m 1}\right) \\
T\left(e_2\right)=a_{12} e_1+a_{22} e_2+\ldots+a_{m 2} e_m=\left(a_{12}, a_{22}, \ldots, a_{m 2}\right) \\
\ldots \\
T\left(e_n\right)=a_{1 n} e_1+a_{2 n} e_2+\ldots+a_{m n} e_m=\left(a_{1 n}, a_{2 n}, \ldots, a_{m n}\right) \\
T(X)=x_1\left[\begin{array}{c}
a_{11} \\
a_{21} \\
\vdots \\
a_{m 1}
\end{array}\right]+x_2\left[\begin{array}{c}
a_{12} \\
a_{22} \\
\vdots \\
a_{m 2}
\end{array}\right]+\ldots+x_n\left[\begin{array}{c}
a_{1 n} \\
a_{2 n} \\
\vdots \\
a_{m n}
\end{array}\right]=\left[\begin{array}{cccc}
a_{11} & a_{12} & \ldots & a_{1 n} \\
a_{21} & a_{22} & \ldots & a_{2 n} \\
& & \vdots & \\
a_{m 1} & a_{m 2} & \ldots & a_{m n}
\end{array}\right]\left[\begin{array}{c}
x_1 \\
x_2 \\
\vdots \\
x_n
\end{array}\right]
\end{gathered}
$$

> [!teorema]
> Qualquer Transformação Linear $T: \mathbb{R}^n \rightarrow \mathbb{R}^m$ pode ser representada por uma matriz $A_{m \times n}$. Isto é,
> 
> $
> [T(X)]=A[X] .
> $

Nós podemos generalizar isso para qualquer base, não apenas para a canônica. Por enquanto, temos o seguinte:
$$
[T(v)]_{e_{\mathbb{R}^{m}}} = A[v]_{e_{\mathbb{R}^{n}}}
$$
Mesmo que não seja de $\mathbb{R}^n$ para $\mathbb{R}^m$, podemos usar um isomorfismo para obter a matriz.


> [!discussao] Termo geral x Representação Matricial.
> Até agora, nós expressávamos as TL pelo termo geral. Por exemplo:
> $
> (x,y,z) \mapsto (2x+y, z+x, y+x, z, z)
> $
> Essa expressão relaciona as **entradas** do vetor arbitrário $(x,y,z)$ do domínio com as **entradas** do vetor $T(x,y,z)$ do contradomínio.
> 
> <br>
> 
> Agora, nós estamos vendo uma forma diferente de representar quaisquer TL: através de uma matriz. O ponto é que, para ser possível representar vetores de EV quaisquer em termos de matrizes colunas, devemos tomar as **coordenadas** dos vetores em relação a alguma base (rever [[Transformações Lineares - conexões]]). 
> 
> Vimos acima isso acontecer para as bases canônicas:
> $
> [T(v)]_{e_{\mathbb{R}^{m}}} = A[v]_{e_{\mathbb{R}^{n}}}
> $
> Agora, no próximo teorema, veremos a generalização disso para quaisquer bases.
> 
> Uma vez de posse de ambos os métodos, podemos calcular as tranformações e os resultados devem mapear os mesmos vetores. Veja o exemplo 1 da minha nota de aula 18.


> [!teorema]
> Seja $T: \mathbb{V} \rightarrow \mathbb{W}$ uma transformação linear, $\mathcal{V}=\left\{v_1, v_2, \ldots, v_n\right\}$ uma base de $\mathbb{V}$ e $\mathcal{W}=\left\{w_1, w_2, \ldots, w_m\right\}$ uma base de $\mathbb{W}$. Definamos a matriz $A_{m \times n}$ onde a i-ésima coluna é dada por $\left[T\left(v_i\right)\right]_{\mathcal{W}}$. Então
> 
> $
> [T(u)]_{\mathcal{W}}=A \cdot[u]_{\mathcal{V}} .
> $
> 
> 
> Tal matriz é chamada de **matriz da transformação linear** $T$ em relação às bases $\mathcal{V}$ e $\mathcal{W}$ e a denotaremos por $[T]_{\mathcal{V} \rightarrow \mathcal{W}}$.
> 
> Obs.: Notações
> - $[T]_{\mathcal{V} \rightarrow \mathcal{W}}=[T]_{\mathcal{W} \leftarrow \mathcal{V}}=[T]_{\mathcal{W}, \mathcal{V}}=[T]_{\mathcal{V}}^{\mathcal{V}}$
> - $[T]_{\mathcal{V} \rightarrow \mathcal{V}}=[T]_{\mathcal{V}}$
> - $[T]_{\mathcal{C} \rightarrow \mathcal{C}}=[T]$ onde $\mathcal{C}$ refere-se a base canônica do respectivo espaço vetorial.

O que nós temos agora é representado a seguir em termos de bases quaisquer:
$$
\begin{gather}
[T(u)]_{\mathcal{W}}=[T]_{\mathcal{V} \rightarrow \mathcal{W}} \cdot[u]_{\mathcal{V}}  \\  \\
[T]_{\mathcal{V} \rightarrow \mathcal{W}} = \begin{bmatrix}
 \\ 
 \left[T\left(v_1\right)\right]_{\mathcal{W}} & \left[T\left(v_2\right)\right]_{\mathcal{W}} & \dots & \left[T\left(v_n\right)\right]_{\mathcal{W}}
 \\ \\
 
\end{bmatrix}_{m \times n}
\end{gather}
$$

Verifiquemos que as contas são as mesmas, tanto pela multiplicação matricial, quanto pela informação da transformação aplicada à base do domínio ("no braço"). Veja o exemplo 2 na minha nota de aula 18.

> [!obs]
> Por isso que, fixada uma Transformação Linear $T: \mathbb{V} \rightarrow \mathbb{W}$, uma base $\mathcal{V}$ no domínio e uma base $\mathcal{W}$ no contradomínio, temos uma matriz que determina essa **tripla** e vice-versa.
> $
> \left(T, \mathcal{V},\mathcal{W} \right) \; \longleftrightarrow \; [T]_{\mathcal{V} \rightarrow \mathcal{W}}
> $
> Se mudarmos um desses três, nossa matriz transformação muda também. 
> 
> **Cuidado:** a definição de $T$ não depende de qual base tomamos, apenas de $\mathbb{V}$ e de $\mathbb{W}$. Só o que muda ao tomar uma base diferente pro dom. ou contradom. é a matriz $[T]$.

> [!exemplo]- Matriz transformação num subespaço vetorial.
> Isso é muito interessante visto que agora podemos usar essa matriz para uma TL num espaço em que não temos as bases canônicas, porque esse espaço pode não ser completo o suficiente para ter a base canônica de alguma coisa. Veja o exemplo do plano na minha nota de aula 18.

> [!exemplo]- Matriz mudança de base.
> Ex. Sejam $\mathcal{V}_1$ e $\mathcal{V}_2$ bases do espaço vetorial $\mathbb{V}$ e seja
> 
> $
> \begin{aligned}
> T: \mathbb{V} & \rightarrow \mathbb{V} \\
> u & \mapsto T(u)=u
> \end{aligned}
> $
> 
> 
> Como podemos interpretar $[T]_{\mathcal{V}_1 \rightarrow \mathcal{V}_2}$ neste caso?
> 
> $
> [u]_{\mathbb{V}_2}=\underbrace{[T]_{\mathbb{V}_1 \rightarrow \mathbb{V}_2}}_{? ? ?} \cdot[u]_{\mathbb{V}_1}
> $
> 
> Bom, se nós montarmos a matriz TL, teremos
> $
> [T]_{\mathcal{V}_{1} \rightarrow \mathcal{V}_2} =\begin{bmatrix}
>  \\ 
>  \left[T\left(v_1\right)\right]_{\mathcal{V}_2} & \left[T\left(v_2\right)\right]_{\mathcal{V}_2} & \dots & \left[T\left(v_n\right)\right]_{\mathcal{V}_2}
>  \\ \\
>  
> \end{bmatrix}
> $
> Como $T(v)=v$, segue que:
> $
> [T]_{\mathcal{V_{1}} \rightarrow \mathcal{V}_2} =\begin{bmatrix}
>  \\ 
>  \left[v_1\right]_{\mathcal{V}_2} & \left[v_2\right]_{\mathcal{V}_2} & \dots & \left[v_n\right]_{\mathcal{V}_2}
>  \\ \\
>  
> \end{bmatrix} = [I]_{\mathcal{V}_{1} \rightarrow \mathcal{V}_2}
> $
> 
> $[T]_{\mathbb{V}_1 \rightarrow \mathbb{V}_2}$ é a **matriz de mudança de base** de $\mathbb{V}_1$ para $\mathbb{V}_2$, que denotamos anteriormente por $[I]_{\mathbb{V}_1 \rightarrow \mathbb{V}_2}$
> 
> Concluímos então que a matriz mudança de base nada mais é do que uma transformação linear particular.

> [!discussao]- Matriz mudança de base e TL.
> Agora, refinando a minha ideia da multiplicação das três matrizes em [[Transformações Lineares - conexões]], temos que
> 
> Seja $T: \mathbb{V} \rightarrow \mathbb{W}$. Logo,
> $
> [T(X)]_{\mathcal{W}} = [T]_{\mathcal{V} \rightarrow \mathcal{W}} \cdot[X]_{\mathcal{V}}
> $
> $
> \begin{aligned} 
> \quad \quad \quad \quad \quad \quad \quad \quad  \quad \quad \quad = \underbrace{[I]_{\mathcal{B} \rightarrow \mathcal{W}}  \;\; \underbrace{[T]_{\mathcal{C} \rightarrow \mathcal{B}} \;\; \underbrace{[I]_{\mathcal{V} \rightarrow \mathcal{C}} \;\; [X]_{\mathcal{V}}}_{[X]_{\mathcal{C}}}}_{[T(X)]_{\mathcal{B}}}}_{[T(X)]_{\mathcal{W}}}
> \end{aligned}
> $


# Propriedades

> [!teorema]
> Considere as transformações lineares $T: \mathbb{V} \rightarrow \mathbb{W}, L: \mathbb{W} \rightarrow \mathbb{U}$ e $\tilde{T}: \mathbb{V} \rightarrow \mathbb{W}$, dada por $\tilde{T}(X)=\sum_{i=1}^k \beta_i T_i(X)$, onde $T_i: \mathbb{V} \rightarrow \mathbb{W}$ são transformações lineares e $\beta_i$ são escalares, e sejam $\mathcal{V}, \mathcal{W}$ e $\mathcal{U}$ bases de $\mathbb{V}, \mathbb{W}$ e $\mathbb{U}$ respectivamente.
> 1. $T$ é invertível $\Leftrightarrow$ a matriz $[T]_{\mathcal{V} \rightarrow \mathcal{W}}$ é invertível. Neste caso
> 
> $
> \left[T^{-1}\right]_{\mathcal{W} \rightarrow \mathcal{V}}=\left([T]_{\mathcal{V} \rightarrow \mathcal{W}}\right)^{-1} .
> $
> 
> 2. $[L \circ T]_{\mathcal{V} \rightarrow \mathcal{U}}=[L]_{\mathcal{W} \rightarrow \mathcal{U}} \cdot[T]_{\mathcal{V} \rightarrow \mathcal{W}}$.
> 3. $[\tilde{T}]_{\mathcal{V} \rightarrow \mathcal{W}}=\sum_{i=1}^k \beta_i\left[T_i\right]_{\mathcal{V} \rightarrow \mathcal{W}}$.

> [!demonstracao]-
> 1. Seja $T: \mathcal{V} \rightarrow \mathcal{W}$ invertível. Queremos mostrar que $A = [T^{-1}]_{\mathcal{W} \rightarrow \mathcal{V}}$ é a matriz inversa de $B = [T]_{\mathcal{V} \rightarrow \mathcal{W}}$.
> 
> Sabemos que para qualquer $w \in \mathcal{W}$, existe um $v \in \mathcal{V}$ tal que $w = T(v)$, o que implica $T^{-1}(w) = v$.
> 
> Aplicando a propriedade da matriz de uma transformação linear:
> 
> $[T^{-1}]_{\mathcal{W} \rightarrow \mathcal{V}} [w]_{\mathcal{W}} = [T^{-1}(w)]_{\mathcal{V}} = [v]_{\mathcal{V}}$
> 
> Chamando $A = [T^{-1}]_{\mathcal{W} \rightarrow \mathcal{V}}$, temos:
> 
> $A [w]_{\mathcal{W}} = [v]_{\mathcal{V}}$
> 
> Como $w = T(v)$, também sabemos pela definição da matriz de $T$ que:
> 
> $[T]_{\mathcal{V} \rightarrow \mathcal{W}} [v]_{\mathcal{V}} = [T(v)]_{\mathcal{W}} = [w]_{\mathcal{W}}$
> 
> Substituindo $[w]_{\mathcal{W}}$ da segunda equação na primeira:
> 
> $A \left( [T]_{\mathcal{V} \rightarrow \mathcal{W}} [v]_{\mathcal{V}} \right) = [v]_{\mathcal{V}}$
> 
> $\left( A \cdot [T]_{\mathcal{V} \rightarrow \mathcal{W}} \right) [v]_{\mathcal{V}} = I \cdot [v]_{\mathcal{V}}$
> 
> Como essa igualdade vale para **todo** vetor $[v]_{\mathcal{V}}$, as matrizes devem ser iguais:
> 
> $A \cdot [T]_{\mathcal{V} \rightarrow \mathcal{W}} = I$
> 
> Portanto, a matriz $[T]_{\mathcal{V} \rightarrow \mathcal{W}}$ é invertível e sua inversa é $A$, ou seja:
> 
> $\left([T]_{\mathcal{V} \rightarrow \mathcal{W}}\right)^{-1} = [T^{-1}]_{\mathcal{W} \rightarrow \mathcal{V}}$


> [!exemplo]- Exemplo do slide 11.
> Esse exemplo é um pouco diferente do que vínhamos lidando. Aqui, nós conhecemos a matriz da TL e queremos a expressão geral de $T(x,y)$, isto é, em função das entradas dos vetores.
> 
> Sabendo que a matriz de uma transformação linear $T: \mathbb{R}^2 \rightarrow \mathbb{R}^3$ nas bases $A=\{(-1,1),(1,0)\}$ do $\mathbb{R}^2$ e $B=\{(1,1,-1),(2,1,0),(3,0,1)\}$ do $\mathbb{R}^3$ é
> 
> $
> [T]_{A \rightarrow B}=\left[\begin{array}{cc}
> 3 & 1 \\
> 2 & 5 \\
> 1 & -1
> \end{array}\right],
> $
> 
> encontre a expressão de $T(x, y)$ e a matriz $[T]$ nas bases canônicas.
> 
> Veja 2 resoluções detalhadas na minha nota de aula 18.