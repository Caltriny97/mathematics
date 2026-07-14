Data Criada: 07/04/2026 às 18:06
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

# Multiplicação por escalar

> [!definicao]
> O produto de uma matriz $A_{m \times n}$ por um número real $\alpha$ é definida como a matriz $C_{m \times n}=\alpha A$ tal que
> 
> $
> c_{i j}=\alpha a_{i j}, \text { ou ainda, }[\alpha A]_{i j}=\alpha[A]_{i j}
> $

> [!comentario]-
> Repare na equivalência na forma de representar as matrizes... 
> $
> A = a_{i j}=[A]_{i j}
> $
> Podemos lidar com as matrizes na forma "pura" $A$ ou então representando o todo na forma de seus elementos genéricos $a_{ij}$. A primeiro igualdade possível por causa dessa equivalência. Já a segunda ingualdade é só uma questão de notação (ambas representam termos quaisquer de $A$).
> 
> É extremamente conveniente mesclar essas duas abordagens nas demonstrações. Ver prova das propriedades de matrizes nas minhas anotações da aula 5.

> [!discussao]- Discussão: Pontes entre Espaço Vetorial e Corpo
> Nós construímos o conjunto das matrizes $\mathbb{M}_{m \times n}$ e definimos operações de soma e produto por escalar de modo conveniente sobre o [[A. Axiomas de Corpo|corpo]] dos reais.
> 
> Em outras palavras, nós criamos **duas pontes iniciais** que ligam matrizes aos reais: as operações de soma e multiplicação por escalar. Eu diria que existe uma terceira: a representação direta de matriz em termos de suas entradas reais, que nos permite tratar as matrizes e as duas operações de modo analítico. Veja **comentário** acima... Não seria algo estritamente necessário, mas facilita nossas contas. 
> 
> Daí, nós mostramos que essa tripla (conjunto, soma e multiplicação por escalar) compõe um [[Espaços Vetoriais e Subespaços Vetoriais|Espaço Vetorial]]. Como fazemos isso? Bom, nós apenas usamos essas pontes para extrapolar as propriedades do nosso corpo dos reais para as matrizes.
> 
> Mas nós não precisamos nos limitar a apenas essas duas pontes. Outros conceitos, como matriz transposta, também são criados através de **pontes** com o nosso corpo. Daí, nós verificamos propriedades (veja [[#Operações matriciais propriedades]]) e comportamento únicos de matrizes que vão muito além dos $8$ axiomas, mas continuam em princípio fazendo uso dessas pontes para extrapolar os conceitos do corpo para o nosso conjunto "novo": as matrizes.
> 
> Vale destacar que essas propriedades são relativas às operações que definimos. Se inventássemos outras operações de soma e multiplicação por escalar, o nosso conjunto poderia nem ser mais um EV, ou ainda que fosse, teria "propriedades extras" diferentes das que estamos vendo agora.


# Propriedades Matriciais

Das nossas definições de soma e multiplicação por escalar, segue que

> [!teorema]
> Sejam $A, B$ e $C \in \mathbb{M}_{m \times n}$ e $\alpha, \beta$ escalares. São válidas as seguintes propriedades:
> 1. $A+B=B+A$
> 2. $(A+B)+C=A+(B+C)$
> 3. $A+\overline{0}_{m \times n}=A$
> 4. Para cada matriz $A \quad \exists!D \in \mathbb{M}_{m \times n}$, tal que $A+D=\overline{0}$. (Not.: $D=-A$ )
> 5. $\alpha(\beta A)=(\alpha \cdot \beta) A$
> 6. $(\alpha+\beta) A=\alpha A+\beta A$
> 7. $\alpha(A+B)=\alpha A+\alpha B$
> 8. $1 A=A$

> [!obs]
> Note que o resultado acima garante que $\mathbb{M}_{m \times n}$ com as operações de soma e produto por escalar usuais, é um [[Espaços Vetoriais|Espaço Vetorial]]. Ex.: Matrizes $\mathbb{M}_{2 \times 3}$ e $\mathbb{M}_{7 \times 5}$ formam espaços vetoriais distintos.
> 
> Porém, o conjunto das Matrizes não constitui um [[Corpo]].

> [!ps]-
> $\mathbb{M}_{m \times n}$ : o conjunto de todas as matrizes de ordem $m \times n$.


# Transposição de Matrizes

> [!definicao]
> A transposta de uma matriz $A_{m \times n}$ é definida como a matriz $C_{n \times m}=A^T$ (ou $A^t$ ) tal que
> 
> $
> c_{i j}=a_{j i}, \text { ou ainda, }\left[A^T\right]_{i j}=[A]_{j i} .
> $

> [!obs]
> Podemos fazer uma associação dos elementos de $\mathbb{R}^n$ com matrizes colunas [ $w$ ] $\in \mathbb{M}_{n \times 1}$ é a matriz coluna cujas entradas correspondem as coordenadas do [[Vetores|vetor]] $w \in \mathbb{R}^n$. Nesta notação, o produto escalar dos vetores $u$ e $v$ de $\mathbb{R}^n$ pode ser visto como o produto de matrizes:
> 
> $
> [u]^t[v] .
> $


# Funções definidas por matrizes (TL)

$f: \mathbb{R}^3 \rightarrow \mathbb{R}^4$ dada por

$$
\begin{gathered}
f(X)=A . X \\
f\left(x_1, x_2, x_3\right)=\underbrace{\left[\begin{array}{lll}
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23} \\
a_{31} & a_{32} & a_{33} \\
a_{41} & a_{42} & a_{43}
\end{array}\right]}_A \cdot \underbrace{\left[\begin{array}{l}
x_1 \\
x_2 \\
x_3
\end{array}\right]}_X=\left[\begin{array}{l}
a_{11} x_1+a_{12} x_2+a_{13} x_3 \\
a_{21} x_1+a_{22} x_2+a_{23} x_3 \\
a_{31} x_1+a_{32} x_2+a_{33} x_3 \\
a_{41} x_1+a_{42} x_2+a_{43} x_3
\end{array}\right]
\end{gathered}
$$


Obs.: $f(\alpha X+\beta Y)=\alpha f(X)+\beta f(Y)$

Ver [[Transformações Lineares]].


# Operações matriciais: propriedades

> [!teorema]
> Sejam $A, B$ e $C$ matrizes com tamanhos apropriados, $\alpha$ e $\beta$ escalares. São válidos as seguintes propriedades:
> 1. A é simétrica se, e somente se, $A=A^T$
> 2. $\left(A^T\right)^T=A$
> 3. $(A+B)^T=A^T+B^T$
> 4. $(\alpha A)^T=\alpha A^T$
> 5. $A \cdot I=A$
> 6. $A \cdot(B+C)=A B+A C$ e $(A+B) \cdot C=A C+B C$
> 7. $(A B) C=A(B C)$
> 8. $\overline{0}_{m \times n} . A_{n \times p}=\overline{0}_{m \times p}$ e $A_{n \times p} . \overline{0}_{p \times q}=\overline{0}_{n \times q}$
> 9. $(A B)^T=B^T A^T$.

> [!demonstracao]-
> 3) $(A+B)^T=A^T+B^T$
> 
> $
> \begin{aligned}
> {\left[(A+B)^T\right]_{i j} } & =[A+B]_{j i} \\
> & =[A]_{j i}+[B]_{j i} \\
> & =\left[A^T\right]_{i j}+\left[B^T\right]_{i j}
> \end{aligned}
> $
> 
> 6) $A(B+C)=A B+A C$
> 
> $
> \begin{aligned}
> {[A(B+C)]_{i j} } & =\sum_{k=1}^p[A]_{i k}[B+C]_{k j} \\
> & =\sum_{k=1}^p[A]_{i k}\left([B]_{k j}+[C]_{k j}\right) \\
> & =\sum_{k=1}^p[A]_{i k}[B]_{k j}+[A]_{i k}[C]_{k j} \\
> & =\sum_{k=1}^p[A]_{i k}[B]_{k j}+\sum_{k=1}^p[A]_{i k}[C]_{k j} \\
> & =[A B]_{i j}+[A C]_{i j}
> \end{aligned}
> $

> [!comentario]-
> A propriedade 5 vale inclusive para matrizes $A$ não quadradas, só temos que prestar atenção na ordem da matriz identidade.
> 
> Esse mesmo raciocínio vale para as demais propriedades: antes de validar e aplicar qualquer uma delas, temos que analisar se as matrizes envolvidas fazem sentido em termos de ordem. Uma simples comutatividade pode tirar a validade de qualquer uma delas. Veja a delicadeza da 7, por exemplo.


# Matriz Inversa

* [[Matriz Inversa]]


# O Determinante

* [[O Determinante]]
