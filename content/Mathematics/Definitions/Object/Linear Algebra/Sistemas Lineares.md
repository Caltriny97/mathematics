Data Criada: 07/04/2026 às 19:24
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

# Dependência Linear

- $\left(\mathbb{R}^2\right.$ ou $\mathbb{R}^2$ ) Dois vetores são paralelos (ou LD ${ }^1$ ): um é múltiplo escalar (ou combinação linear) do outro

$$
v=\alpha u
$$

- $\left(\mathbb{R}^3\right)$ Três vetores são coplanares (ou LD): um é combinação linear dos demais

$$
v=\alpha u+\beta w+\gamma z
$$
$$
\left\{\begin{array}{l}
v_1=\alpha \boldsymbol{u}_1+\beta \boldsymbol{w}_1+\gamma z_1 \\
v_2=\alpha \boldsymbol{u}_2+\beta \boldsymbol{w}_2+\gamma z_2 \\
v_3=\alpha \boldsymbol{u}_3+\beta \boldsymbol{w}_3+\gamma z_3
\end{array}\right.
$$

> [!ps]
> ${ }^1$ Linearmente Dependentes - veremos formalmente este conceito adiante.


# Introdução

> [!problema]
> Ver problema 1 de [[planos]]

> [!discussao] Entendendo um caso simples.
> 
> Normalmente, nós somamos uma eq. com a outra para isolar uma variável numa única eq. O ponto é: por quê fazer essas substituições, somando uma eq. com múltiplo da outra de modo a "sumir" com uma delas resolve o nosso problema? Afinal, nós estaremos recebendo uma terceira eq. que, a princípio, nada tem a ver com as duas anteriores.
> 
> Enfim, como que essa terceira eq. ou reta (vendo geometricamente) pode ser equivalente às outras duas retas?
> 
> **É uma combinação linear das outras duas!**
> 
> Quando fazemos a conta, o nosso primeiro passo é achar um sistema equivalente (quem são equivalentes são os **sistemas** e não as retas, equações em si). Depois, nós fazemos um abuso de notação e esquecemos de uma das eq. (mas ela continua lá). Ver minhas anotações para melhor entendimento.
> 
> O ponto é: quando realizamos essas operações elementares nas nossas eq. iniciais, obtemos retas mais alinhadas com os eixos cartesianos (não é que as retas sejam equivalentes, mas o seu ponto de interseção não muda). Quando chegamos na forma escalonada reduzida, temos um sistema equivalente, com retas perpendiculares aos eixos, nos permitindo ver com facilidade as coordenadas da interseção (que se manteve a mesma o tempo todo, e não as retas).
> 
> O sistema inicial e escalonado (final) não representam geometricamente a mesma coisa, mas o conjunto solução ainda é o mesmo.

> [!comentario]
> No caso mencionado na discussão acima, lidamos com $2$ retas se estamos em duas dimensões. Por outro lado, lidamos com $2$ planos se estivermos em três dimensões. Daí não teríamos uma única solução, mas sim infinitas com a variável $z$ livre.
> 
> quem são equivalentes são os **sistemas** e não as retas, equações em si.

# Definição de SL

> [!definicao]
> Um Sistema de Equações Lineares com $m$ equações e $n$ incógnitas é um conjunto de equações do tipo:
> 
> $
> \left\{\begin{array}{l}
> a_{11} x_1+a_{12} x_2+\ldots+a_{1 n} x_n=b_1 \\
> a_{21} x_1+a_{22} x_2+\ldots+a_{2 n} x_n=b_2 \\
> \ldots \\
> a_{m 1} x_1+a_{m 2} x_2+\ldots+a_{m n} x_n=b_m
> \end{array}\right.
> $
> 
> $\operatorname{com} a_{i j} \in \mathbb{R}$ para todo $i=1, \ldots, m$ e $j=1, \ldots, n$.


# Operações Elementares

> [!teorema]
> Se aplicarmos um número finito de operações elementares a um Sistema Linear, então o Sistema Linear obtido será equivalente ao original (terão as mesmas soluções).

> [!definicao]
> Uma **operação elementar** sobre as **equações de um Sistema Linear** é uma das seguintes operações:
> 1. Multiplicar uma equação por um escalar não nulo.
> 2. Permutar duas equações.
> 3. Adicionar a uma equação um múltiplo escalar de outra equação.

> [!discussao]
> 


# Sistemas Lineares: Representação Matricial

$$
\begin{array}{llc}
\left\{\begin{array}{l}
x+2 y=1 \\
2 x+y=0
\end{array}\right. & \xrightarrow{\text { Op. Elementares sobre as equações DO SL }} & \left\{\begin{array}{l}
x=-\frac{1}{3} \\
y=\frac{2}{3}
\end{array}\right. \\
{\left[\begin{array}{ll|l}
1 & 2 & 1 \\
2 & 1 & 0
\end{array}\right]} & \xrightarrow{\text { Op. Elementares sobre as linhas da Matriz }} & {\left[\begin{array}{ll|l}
1 & 0 & -1 / 3 \\
0 & 1 & 2 / 3
\end{array}\right]}
\end{array}
$$

> [!definicao]
> Uma **operação elementar** sobre as **linhas de uma matriz** é uma das seguintes operações:
> 1. Multiplicar uma linha da matriz por um escalar não nulo.
> 2. Permutar duas linhas da matriz.
> 3. Adicionar a uma linha da matriz um múltiplo escalar de outra linha da matriz.

Todo sistema linear pode ser representado na forma $AX=B$ e vice versa.


# Forma Escalonada Reduzida

> [!definicao]
> Uma matriz $A_{m \times n}$ está na forma escalonada-reduzida se:
> * a) Todas a linha nulas ocorrem abaixo das linhas não-nulas.
> * b) O pivô (primeiro elemento não nulo) de cada linha não-nula é 1 .
> * c) O pivô de cada linha não nula ocorre à direita do pivô da linha anterior.
> * d) Se uma coluna contem pivô, então os demais elementos desta coluna são nulos.

O escalonamento se dá pelo método de Gauss-Jordan, que consiste em, **coluna por coluna**, realizar operações elementares para "formar" o pivô da coluna e zerar os demais elementos da coluna.

> [!definicao]
> A matriz $M_1$ é dita equivalente por linhas a matriz $M_2$ se a matriz $M_2$ pode ser obtida de $M_1$ aplicando-se um número finito de operações elementares.

> [!teorema]
> Toda matriz $M$ é equivalente por linhas a uma única matriz escalonada reduzida.

> [!comentario]
> Ver ideia da demonstração deste teorema no slide da aula 6. É interessante porque a prova é feita usando o próprio método de escalonamento. 


# Quantas soluções pode ter um Sistema Linear?

Ver discussão das minhas notas da Unesp e comparar com o slide.


É possível ter exatamente $2$ soluções distintas? **Não!**

Sejam $X_1$ e $X_2$ soluções distintas de $A X=B$. Para qualquer $\lambda \in \mathbb{R}$ teremos

$$
\begin{aligned}
A\left(\lambda X_1+(1-\lambda) X_2\right) & =A\left(\lambda X_1\right)+A\left((1-\lambda) X_2\right) \\
& =\lambda\left(A \cdot X_1\right)+(1-\lambda)\left(A \cdot X_2\right) \\
& =\lambda(B)+(1-\lambda)(B) \\
& =B
\end{aligned}
$$


Logo $A X=B$ terá infinitas soluções.

> [!teorema]
> Teorema: Um Sistema Linear pode ter zero, uma única ou infinitas soluções.

Veja relação entre [[Matriz inversa e o SL]].


# Análise das soluções

Ex.

$$
\begin{gathered}
\left\{\begin{array}{l}
x_1+x_2+3 x_3-3 x_4=0 \\
2 x_2+x_3-3 x_4=0 \\
x_1+2 x_3-x_4=-1
\end{array}\right. \\
{\left[\begin{array}{cccc|c}
1 & 1 & 3 & -3 & 0 \\
0 & 2 & 1 & -3 & 3 \\
1 & 0 & 2 & -1 & -1
\end{array}\right] \longrightarrow \cdots \longrightarrow\left[\begin{array}{cccc|c}
1 & 0 & 0 & 1 & 1 \\
0 & 1 & 0 & -1 & 2 \\
0 & 0 & 1 & -1 & -1
\end{array}\right]} \\
\text { Solução: }\left[\begin{array}{c}
1-x_4 \\
2+x_4 \\
-1+x_4 \\
x_4
\end{array}\right] \forall x_4 \in \mathbb{R}
\end{gathered}
$$

Claro que, como temos menos equações que incógnitas, 1 variável livre no caso, vamos ter a solução do sistema em função dessa única variável livre.

Se fosse o contrário, haveria mais **restrição** (equação) do que incógnitas. Isso se manifesta na forma escalonada reduzida através de linha(s) zerada(s). Se todas essas eq. a mais estiverem também zeradas do lado direito da barra, a solução será a mesma das eq. com pivôs. Se pelo menos uma dessas eq. a mais tiver um valor diferente de zero no lado direito da barra, o sistema será impossível.

**Resumindo...** Verificamos a natureza da solução em $3$ passos:
* (i) Se houver alguma linha nula com o lado direito $\neq$ de zero, o SL é impossível. 
* (ii) Visto isso, se a FER for a matriz identidade (não importa se têm mais linhas nulas embaixo), a solução é única. 
* (iii) Por fim, se não se enquadrar em nenhum dos casos, é indeterminado.


# Sistema Linear Homogêneo

> [!definicao]
> Um Sistema Linear da forma $A X=\overline{0}$ é chamado de Sistema Linear Homogêneo.

> [!teorema]
> Considere um Sistema Linear Homogêneo $A X=\overline{0}, \operatorname{com} A_{m \times n}$. São válidas as seguintes propriedades:
> 1. $X=\overline{0}_{n \times 1}$ é uma solução.
> 2. Se $X_1$ e $X_2$ são soluções, então $X_1+X_2$ também é.
> 3. Se $X$ é solução, então $\lambda X$ também é solução para todo $\lambda \in \mathbb{R}$.
> 
> **Prova:**
> 1. $A_{m \times n} \overline{0}_{n \times 1}=\overline{0}_{m \times 1}$
> 2. $A\left(X_1+X_2\right)=A X_1+A X_2=\overline{0}+\overline{0}=\overline{0}$
> 3. $A(\lambda X)=\lambda(A X)=\lambda \overline{0}=\overline{0}$


> [!proposicao]
> Considere as operações usuais de $\mathbb{M}_{n \times 1}$ e $A$ uma matriz de ordem $m \times n$. Então o conjunto solução do sistema linear homogêneo $A X=\overline{0}$ é um [[Espaços Vetoriais|espaço vetorial]].
> 
> Ver demonstração em [[Espaços e Subespaços Vetoriais]].
