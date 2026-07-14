Data Criada: 09/04/2026 às 20:41
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

Qual a condição para que $A_{n\times n}$ seja invertível (não-singular)? ($AX=B$ solução única, veja [[Matriz inversa e o SL]])

Veja a análise do slide 8.
Estamos interessados em saber as condições que a matriz precisa respeitar para ser invertível. Para isso, o melhor é analisar o processo de escalonamento da matriz $A$. Ela somente será invertível (ou o sistema $AX=B$ só terá solução) se for possível escaloná-la até $I$.

No slide, vemos no caso $2\times 2$ que, não importa o caso que estamos analisando ($a_{11} \neq 0$ ou $a_{11}=0$), a matriz será invertível se o **determinante** for $\neq 0$. Em outras palavras, olhar o determinante está nos garantindo se $A$ é ou não invertível.

Esse raciocínio pode ser generalizado para os demais casos.

> [!container]- Analisando o escalonamento...
> Caso $n=1$
> $
> A_{1 \times 1}=[a]: \quad a \neq 0
> $
> 
> Caso $n=2$
> - $A_{2 \times 2}=\left[\begin{array}{ll}a_{11} & a_{12} \\ a_{21} & a_{22}\end{array}\right] a_{11} a_{22}-a_{21} a_{12} \neq 0$
> - Se $a_{11} \neq 0$ :
> 
> $
> \xrightarrow{L_2 \rightarrow a_{11} L_2}\left[\begin{array}{cc}
> a_{11} & a_{12} \\
> a_{11} a_{21} & a_{11} a_{22}
> \end{array}\right] \xrightarrow{L_2 \rightarrow L_2-a_{21} L_1}\left[\begin{array}{cc}
> a_{11} & a_{12} \\
> 0 & \underbrace{a_{11} a_{22}-a_{21} a_{12}}_{\neq 0}
> \end{array}\right]
> $
> 
> - Se $a_{11}=0$ :
> 
> $
> \left[\begin{array}{cc}
> 0 & a_{12} \\
> a_{21} & a_{22}
> \end{array}\right] \xrightarrow{L_1 \rightarrow L_2}\left[\begin{array}{cc}
> a_{21} & a_{22} \\
> 0 & a_{12}
> \end{array}\right] \quad a_{21} a_{12} \neq 0
> $
> 
> Caso $n=3$
> $
> \begin{aligned}
> & A_{3 \times 3}=\left[\begin{array}{lll}
> a_{11} & a_{12} & a_{13} \\
> a_{21} & a_{22} & a_{23} \\
> a_{31} & a_{32} & a_{33}
> \end{array}\right]: \\
> & a_{11}\left(a_{22} a_{33}-a_{23} a_{32}\right)-a_{12}\left(a_{21} a_{33}-a_{23} a_{31}\right)+a_{13}\left(a_{21} a_{32}-a_{22} a_{31}\right) \neq 0
> \end{aligned}
> $

O determinante surgiu por diferentes contextos e um deles é esse contexto algébrico de mostrar se uma matriz é ou não invertível.


# (Uma possível) Definição de determinante

> [!definicao]
> Seja $A_{n \times n}$ uma matriz quadrada qualquer. O determinante de $A$ é um escalar definido por
> 
> $
> \operatorname{det}(A)= \begin{cases}a_{11} & \text { se } n=1 \\ \sum_{j=1}^n a_{1 j} \tilde{a}_{1 j} & \text { se } n \geqslant 2\end{cases}
> $
> 
> onde
> - $\tilde{a}_{i j}$ é o cofator do elemento $a_{i j}$ : $\tilde{a}_{i j}=(-1)^{i+j} \operatorname{det}\left(\tilde{A}_{i j}\right)$
> - $\tilde{A}_{i j}$ é a matriz menor a matriz de ordem $(n-1) \times(n-1)$ obtida de $A$ removendo-se a i-ésima linha e a j-ésima coluna.
> 
> 
> **Obs.:** O determinante também pode ser definido como um funcional multilinear alternado que vale 1 quando aplicado na identidade.

Essa definição, por ser via recorrência, vai dizer muito de como vamos provar certos resultados mais a frente via recorrência também (indução).


# Teorema de Laplace

> [!teorema]
> O determinante de uma matriz quadrada $A_{n \times n}$ pode ser calculado fazendo-se o desenvolvimento por qualquer linha ou qualquer coluna de $A$. (Indução ou propriedades da próxima sessão)


# Propriedades

> [!teorema]
> Sejam A e $B$ matrizes $n \times n$.
> 1) $\operatorname{det}\left[\begin{array}{c}A_1 \\ A_2 \\ \cdots \\ \alpha X+\beta Y \\ \cdots \\ A_n\end{array}\right]=\alpha \operatorname{det}\left[\begin{array}{c}A_1 \\ A_2 \\ \cdots \\ X \\ \cdots \\ A_n\end{array}\right]+\beta \operatorname{det}\left[\begin{array}{c}A_1 \\ A_2 \\ \cdots \\ Y \\ \cdots \\ A_n\end{array}\right]$. **(indução)**
> 2) Se $A$ possui duas ou mais linhas (ou colunas) iguais, então $\operatorname{det}(A)=0$. **(indução)**
> 3) Se $B$ é obtida de $A$ multiplicando-se uma linha por um escalar $\alpha$, então $\operatorname{det}(B)=\alpha \operatorname{det}(A)$ **(1)**
> 4) Se $B$ resulta de $A$ pela troca de duas linhas distintas então $\operatorname{det}(B)=-\operatorname{det}(A)$. **(1 e 2)**
> 5) Se $B$ é obtida de $A$ substituindo-se a linha $I$ por ela somado a um múltiplo escalar de outra linha, então $\operatorname{det}(A)=\operatorname{det}(B)$. **(1 e 2)**
> 6) $\operatorname{det}(A B)=\operatorname{det}(A) \operatorname{det}(B)$. **(matrizes elementares)**
> 7) $\operatorname{det}\left(A^{\top}\right)=\operatorname{det}(A)$. **(matrizes elementares)**
> 8) Se $A$ possui uma linha (ou coluna) nula, então $\operatorname{det}(A)=0$. **(indução)**
> 9) Se $A$ é triangular (superior ou inferior), então $\operatorname{det}(A)=\prod_{i=1}^n a_{i i}$. **(induçāo)**
> 10) $A$ invertível se, e somente se, $\operatorname{det}(A) \neq 0$. **(3), (4) e (5) ou (6)**
> 11) Se $A$ é invertível então $\operatorname{det}\left(A^{-1}\right)=\frac{1}{\operatorname{det}(A)}$. **(6)**
> 
> Ao lado de cada propriedade, estão as ideias para prová-las. Tem alguns que podem ser provados pelas propriedades das matrizes elementares também. Veja algumas demonstrações na minha nota de aula 8.

> [!obs]
> As propriedades $(3), (4)$ e $(5)$ falam justamente da influência das [[operações elementares]] sobre o determinante da matriz.
> 
> **A sacada aqui é:**
> Ao escalonar uma matriz $A$ até em $R=I$, o que podemos falar sobre $\det(A)$? Bom, como $\det(I)=1$ (provar por indução), podemos afirmar que $\det(A) \neq 0$ devido à natureza das propriedades $(3), (4)$ e $(5)$ conforme vimos. 
> 
> É por isso que usamos o determinante para verificar invertibilidade (rever [[Matriz Inversa]]).

> [!comentario]
> A propriedade $(6)$ tem tudo a ver com a propriedade do produto de matrizes do teorema 1.3 de [[Matrizes]], que fala $(A B)^{-1}=B^{-1} A^{-1}$ se $A$ e $B$ são invertíveis.
> 
> Para provar a parte de propriedade (2) sobre colunas iguais, usamos a propriedade (7). Temos que ter cuidado em usar propriedades a posteriori, pois pode ser que elas dependam do que está antes. Mas, como a (7) usa matrizes elementares, então não tem problema.


Normalmente, coisas recursivas podem ser provadas por indução. Por isso, várias das nossas demonstrações caíram em provas por indução, devido à definição recursiva que foi dado ao determinante.


> [!teorema]
> Considere as matrizes $A_{r \times r}, B_{r \times(n-r)}, C_{(n-r) \times(n-r)}$ e $\overline{0}_{(n-r) \times r}$, com $\overline{0}$ denotando uma matriz nula e $n>r$. Então é válido que
> 
> $
> \operatorname{det}\left[\begin{array}{ll}
> A & B \\
> \overline{0} & C
> \end{array}\right]=\operatorname{det}(A) \cdot \operatorname{det}(C) .
> $

Veja a demonstração desse teorema no slide 8.