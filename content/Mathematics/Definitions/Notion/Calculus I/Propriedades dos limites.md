
Data Criada: 30/05/2026 às 23:17
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

Sabemos alguns limites e combinando-os com essas propriedades, podemos calcular outros limites. Mas **cuidado**: só podemos aplicar as propriedades dos limites se soubermos que o limite das partes existem (por isso o conceito de [[Continuidade]] é tão importante)

> [!obs]
> Além de sabermos que o limite existe, temos que tomar cuidado para não cair em nenhum caso de **indeterminação**. 
> 
> As propriedades que vamos ver abaixo só valem quando as sequências convergem para algum valor **determinado** (real). 
> 
> Quando lidamos com indeterminações, não sabemos como a sequência se comporta, portanto não podemos tirar muitas conclusões. Ver problema 5.b da lista 11.

> [!teorema] Linearidade.
> Sejam $\left(x_n ; n \in \mathbb{N}\right)$, $\left(y_n ; n \in \mathbb{N}\right)$ sequências tais que $\lim_{ n \to \infty }x_{n}=x$, $\lim_{ n \to \infty }y_{n}=y$. Sejam, $a,b \in \mathbb{R}$. Temos que
> $
> \lim_{ n \to \infty } (ax_{n}+by_{n})=ax+by
> $

> [!demonstracao]-
> Na nota de aula 11, o Milton usou desigualdade triangular para chegar na seguinte expressão:
> $
> |ax_{n}+by_{n}-ax-by|\leqslant |a| |x_{n}-x|+|b||y_{n}-y|
> $
> Interpretando esse resultado, podemos calcular o limite do termo da direita para nichar o da esquerda. A partir disso, podemos tirar duas conclusões ao analisar só o termo da direita.
> 
> * Podemos concluir que é suficiente considerar o caso $a,b \geqslant 0$, uma vez que eles estão em módulo.
> * A próxima sacada consiste em fazer uma troca de variáveis. Definiremos $u_{n}=|x_{n}-x|$ e $v_{n}=|y_{n}-y|$. Sabendo que $\lim_{n\rightarrow\infty} x_{n} = x$ e $\lim_{n\rightarrow\infty} y_{n} = y$, o limite dessas novas sequências será:
> 	- $\lim_{n\rightarrow\infty} u_{n} = 0$
> 	- $\lim_{n\rightarrow\infty} v_{n} = 0$
> 
> * Além disso, por estarem dentro de um módulo, $u_{n}$ e $v_{n}$ são **sequências não-negativas**.
> * Para manter a notação concisa, o Milton apenas manteve $x_n=u_n$ e $y_n=v_n$.
>   
> Ver minha versão mais detalhada: [[demonstração da linearidade dos limites.pdf]]  

> [!obs]
> Conforme dito logo acima, só podemos aplicar linearidade do limite quando sabemos que $a_n$ e $b_n$ têm limites. Eles poderiam não ter limites e terem diferença zero mesmo assim (ex.: duas $f$ oscilantes de $+1$ e $-1$).

> [!teorema] Multiplicatividade.
> 1.
> $
> \lim_{ n \to \infty }x_{n}y_{n}=xy
> $
> 2. Se $y_n \neq 0$ para todo $n \in \mathbb{N}$, e $y \neq 0$, então
> $
> \lim_{ n \to \infty } \frac{x_{n}}{y_{n}} = \frac{x}{y}
> $

> [!teorema] Monotonicidade.
> Sejam $\left(x_n ; n \in \mathbb{N}\right),\left(y_n ; n \in \mathbb{N}\right)$ sequências tais que
> 
> $
> \lim _{n \rightarrow \infty} x_n=x \; \text { e } \lim _{n \rightarrow \infty} y_n=y .
> $
> 
> 
> Se $x_n \leq y_n$ para todo $n \in \mathbb{N}$, então $x \leq y$.

> [!teorema] Teorema do Sanduíche
> Sejam $\left(x_n ; n \in \mathbb{N}\right)$, $\left(y_n ; n \in \mathbb{N}\right)$, $\left(z_n ; n \in \mathbb{N}\right)$ tai que $x_n \leqslant y_n \leqslant z_n$ para todo $n \in \mathbb{n}$, e $\lim_{ n \to \infty }x_{n}=a=\lim_{ n \to \infty }z_{n}$, então
> $
> \lim_{ n \to \infty }y_{n} = a
> $

É assim que provamos a maior parte dos limites. Nós temos um banco de sequências com as quais a gente sabe qual é o limite e depois nós as utilizamos para sanduichar o limite que queremos calcular. 

Usualmente, nós tiramos a diferença e pegamos o módulo, i.e., a sequência de baixo torna-se constante igual a zero e a de cima é uma que vai para zero. Em outras palavras, é muito comum, ao usar teorema do sanduíche, uma das sequências ser constante.

Ver demonstração do [[O Teorema Fundamental do Cálculo]] para ver como o teorema do sanduíche se aplica às distâncias (de fora e de dentro) e não às sequências por si só.

> [!obs]-
> Da mesma forma que a variável de integração não pode estar no resultado, aqui em limites não podemos ter o $n$ no resultado final. Isso é porque podemos trocar a variável por qualquer coisa e o resultado não deve se alterar.

