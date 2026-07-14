Data Criada: 07/06/2026 às 11:26
Tags:

Tipos:
Exemplos:
Construções: 
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas: [[Fórmula de mudança de variáveis]]

# Introdução

Conforme discutido em [[Fórmula de mudança de variáveis]], a função $\cfrac{1}{x}$ é uma função racional que não é derivada de nenhuma outra função racional. Notemos que para $x,y>0$,
$$
|f(y)-f(x)|=\left|\frac{1}{y}-\frac{1}{x}\right|=\left|\frac{ x-y}{x y}\right| \leqslant \frac{|y-x|}{x y} .
$$

Logo, para $x, y \in[a, b]$ com $a>0$ e $b>a$,

$$
|f(y)-f(x)| \leqslant \frac{|y-x|}{a^2},
$$

pelo que $f$ é Lipschitz e em particular integrável.


# Definição

A função logaritmo é a única que satisfaz duas propriedades: (i) sua derivada é $\cfrac{1}{x}$ e (ii) vale zero para $x=1$.

> [!definicao] Definição.
> A função **logaritmo** é a função log: $(0,+\infty) \rightarrow \mathbb{R}$ dada por
> $
> \log x=\int_1^x \frac{d y}{y}
> $
> para todo $x \in(0,+\infty)$.

Em outras palavras...
$$
\log(x) :=
\begin{cases}
\int_{1}^{x}{ \frac{1}{y} \, dy}  \\ \\ 
- \int_{x}^{1}{ \frac{1}{y} dy}
\end{cases}
$$


**Obs.**
Pelo [[O Teorema Fundamental do Cálculo|TFC]],
$$
\frac{d}{dx}\log x = \frac{1}{x}
$$
O logaritmo é uma **primitiva** (anti-derivada) da função $\frac{1}{x}$.

> [!corolario]
> Terminando o que começamos em [[Fórmula de mudança de variáveis]], segue que
> $
> \int tg \, dx = -\log \cos(x) + C 
> $
> Para tirar a prova real, basta tomar a derivada do resultado.


# Propriedades

A função logaritmo tem várias propriedades importantes. A continuação veremos algumas delas

> [!container] Passo inicial...
> Primeiro, provaremos um resultado:
> Pela definição de $\log$ e usando a convenção de sinal negativo para intervalos na integral, temos que
> $
> \log y -\log x = \int_{x}^{y}  \, \frac{dz}{z}
> $
> Pelo que $\log x < \log y$. Além disso, se multiplicarmos ambos os lados por $\cfrac{1}{y-x}$, teremos que
> $
> \frac{\log y -\log x}{y-x} = \frac{1}{y-x} \int_{x}^{y}  \, \frac{dz}{z}
> $
> Mas, pelo [[O primeiro teorema do valor médio (integrais)|TVM (integrais)]], temos que (poderíamos usar [[Teorema do Valor Médio|TVM]] junto de [[O Teorema Fundamental do Cálculo|TFC]] e daria no mesmo)
> $
> \frac{1}{z} = \frac{1}{y-x} \int_{x}^{y}  \, \frac{dz}{z}
> $
> para algum $x \leqslant z \leqslant y$. Atenção, pois a $f(z)$ do enunciado do teorema aqui não é $\log(z)$, mas sim $\cfrac{1}{z}$. Portanto, como $\cfrac{1}{y} \leqslant \cfrac{1}{z} \leqslant \cfrac{1}{x}$, temos que
> $
> \begin{gather}
> \frac{1}{y} \leqslant \frac{\log y -\log x}{y-x} \leqslant \frac{1}{x} \iff \\ \\ \log x+\frac{y-x}{y} \leqslant \log y \leqslant \log x + \frac{y-x}{x} 
> 
> \end{gather}
> $
> **Exercício:** provar cotas mais precisas usando a fórmula de Taylor com resto integral.


> [!container] (i) É estritamente crescente e contínua.
> Pelo que vimos no quadro anterior,
> $
> \log y -\log x = \int_{x}^{y}  \, \frac{dz}{z}
> $
> Então, se o argumento cresce, o intervalo de integração cresce e o resultado acima cresce estritamente, uma vez que trata-se de uma função sempre positiva.
> 
> Logo, a função logaritmo é estritamente crescente e contínua. Portanto, a **inversa** de $\log$, que denotaremos por 
> $\exp = \log ^{-1}$
> está bem definida (num intervalo fechado). 
> 
> Lembremos que funções estritamente crescentes e contínuas têm inversas também estritamente crescentes e contínuas. Como supomos que a função. Lembre problema 3.a da lista 9.
> 
> Antes de ver qual é o domínio de $\exp$, que é simplesmente a imagem de $\log$, provaremos outras propriedades de $log$. 


> [!container] (ii) É Lipschitz.
> Portanto, é **contínua**.


> [!container] Produto do logaritmo é a soma dos logaritmos.
> Sejam $a,x > 0$. Temos que
> 
> $
> \begin{aligned}
> \log (a x) & =\int_1^{a x} \frac{d y}{y}=\int_{1 / a}^x \frac{a d z}{a z}=\int_{1 / a}^1 \frac{d z}{z}+\int_1^x \frac{d z}{z} =-\log (1 / a)+\log x
> \end{aligned}
> $
> Usamos aqui [[Fórmula de mudança de variáveis]], trocando os limites de integração à nova variável.
> 
> Por outra parte
> 
> $
> \int_1^{1 / a} \frac{d x}{x}=\int_a^1 \frac{d y}{a} \cdot \frac{a}{y}=-\int_1^a \frac{d y}{y},
> $
> 
> pelo que $\log (1 / a)=-\log a$ e
> 
> $
> \log (a x)=\log a+\log x \text {. }
> $
> podíamos também substituir $x=1$, já que $\log 1 =0$


> [!container] Contante de Euler.
> Queremos provar agora que existe um número real $x_0$ tal que $\log x_0 =1$. Para isso, usaremos o [[Teorema do Valor Intermediário]]. Mas antes, temos que
> 
> $
> \log n = \int_1^n \frac{d x}{x}=\sum_{i=1}^{n-1} \int_i^1 \frac{d x}{x} \geqslant \sum_{i=1}^n \frac{1}{i+1}
> $
> Estamos dividindo o intervalo $[1,n]$ em intervalinhos unitários. Pela monotonicidade da integral, é maior ou igual do que o menor valor da função no intervalo correspondente. A função $\cfrac{1}{x}$ é decrescente, portanto o menor valor dela é o valor atingido no extremo direito do intervalo.
> 
> 
> Logo, $\log 4 \geqslant 1 / 2+1 / 3+1 / 4=13 / 12$. Como $\log 1=0$ e o logaritmo é contínuo, existe $x_0 \in (1,4)$ tal que
> $
> \log x_0=1 
> $
> Como $\log$ é crescente, $x_{0}$ é único.
> 
> A constante $x_0$ se denota por $e$, e é conhecida como a **constante de Euler**. Notemos que para todo $n \in \mathbb{N}$
> 
> $
> \begin{aligned}
> \log \left(e^n\right) & =\log \left(e \cdot e^{n-1}\right)=\log (e)+\log \left(e^{n-1}\right) \\
> & =1+\log \left(e^{n-1}\right)=\ldots \\
> & =n .
> \end{aligned}
> $
> 
> Em outras palavras, definimos $e$ como o único zero da função $\log(x)-1$.


> [!container] Domínio da função exponencial.
> Pelo [[Teorema do Valor Intermediário|TVI]], para todo $x>0$ existe $y>0$ tal que
> 
> $
> x=\log y .
> $
> Todo número positivo está na imagem da função logaritmo, porque todo número natural está na imagem, em particular $0$ e $n$. Pelo TVI, todos os números entre $0$ e $n$ também estão na imagem.
> 
> Como $\log (1 / y)=-x$, vemos que $\operatorname{Im}(\log )=\mathbb{R}$, pelo que  $\exp :\mathbb{R} \rightarrow(0,+\infty)$ está bem definida. Observemos que como $\log (a b)=\log (a)+\log (b)$,
> 
> $
> \begin{gather}
> \log(\;\exp(a)\exp(b)\;)=\log(\;\exp(a)\;)+\log(\;\exp(b)\;)=a+b \quad /\exp \\ \\
> \exp( \; \log(\exp(a)\exp(b)) \;)=\exp(a+b) \\ \\
> \exp(a)\exp(b)=\exp(a+b)
> \end{gather}
> $
> 
> Em outras palavras, a função exponencial é **multiplicativa**. 

Agora vamos provar que a exponencial é de fato o que esperamos: a função potência. O ponto aqui é: nós simplesmente definimos a função $\exp$ como a inversa da função $\log$, então ainda não sabemos nada se isso têm a ver com [[a função potência]].

> [!teorema]
> Para todo $x \in \mathbb{R}$,
> $
> \exp(x) = e^x
> $

> [!demonstracao]-
> Aqui, usaremos a mesma ideia que usamos para extender **a função potência** aos reais. Só que agora vai ser mais fácil porque sabemos a priori que a função exponencial é contínua.
> 
> Ver nota de aula 21 do Milton.
> 
> Lá foi feito o seguinte passo a passo:
> * mostramos que $\exp(n) = e^n$ para os números inteiros. Isso é simplesmente a inversa do que resultado que mostramos acima: $\log(e^n)=n$
> * em seguido mostramos que $\exp(\cfrac{p}{q} = e^\frac{p}{q})$, a partir da $q$-ésima raiz de $e^p$. Logo, $\exp(e^x)=e^x$ para todo $x \in \mathbb{Q}$
> * temos, portanto, duas funções contínuas que coincidem nos números racionais: [[a função potência]] e a função exponencial
> * Através do lema abaixo, concluímos que elas sao iguais.

> [!lema]
> Sejam $f, g:[a, b] \rightarrow \mathbb{R}$ contínuas. Se
> 
> $
> f(x)=g(x)
> $
> 
> para todo $x \in \mathbb{Q} \cap[a, b]$, então $f=g$.

> [!demonstracao]-
> Seja $x \in[a, b]$ e seja $\left(x_n ; n \in \mathbb{N}\right)$ em $Q \cap[a, b]$ Tal que $\lim _{n \rightarrow \infty} x_n=x$. Temos que
> 
> $
> f(x)=\lim _{n \rightarrow \infty} f\left(x_n\right)=\lim _{n \rightarrow \infty} g\left(x_n\right)=g(x) .
> $
> 
> A primeira e última igualdades vêm da continuidade das funções. A segunda, por outro lado, é uma igualdade do que está dentro dos limites.
> 
> Nós já sabemos na aula de [[a função potência]] que qualquer número irracional pode ser aproximado por números racionais quando tomados os limites.


> [!resumo]-
> O cálculo é um campo da matemática que nos permite fazer umas definições meio inesperadas:
> 
> Nòs começamos definindo o **logaritmo** como a primitiva antiderivada da função $\cfrac{1}{x}$. A **função exponencial**, por outro lado, é a função inversa do logaritmo. E agora, miraculosamente, a **função exponencial** vai ser a mesma coisa que a função potência quando escolhemos $a = e$.


# Derivada da exponencial

Como exp $=\log _1^{-1}$ podemos usar a fórmula da derivada da função inversa para calcular a derivada da função exponencial. Temos que
$$
\exp ^{\prime}(x)=\frac{1}{\log ^{\prime}(\exp (x))}=\frac{1}{1 / \exp (x)},
$$
pelo que $\exp ^{\prime}(x)=\exp (x)$. En outros palavras,
$$
\frac{d}{d x} e^x=e^x
$$

A função exponencial é a única função que satisfaz essa propriedade e tal que vale $1$ em zero. Não provaremos ainda que ela é a única... (faremos isso com a fórmula de Taylor).

> [!obs]
> $
> e = \lim_{ n \to \infty } \left( 1+ \frac{1}{n} \right)^{n} \implies e = \sum_{n=0}^{\infty} \frac{1}{n!} := \lim_{ n \to \infty } \sum_{n=0}^{N} \frac{1}{n!}
> $

> [!lema]
> Seja $P: \mathbb{R} \rightarrow \mathbb{R}$ um polinômio. Temos que
> $
> \lim_{ N \to \infty } P(N)e^{-N}=0
> $

> [!demonstracao]-
> * primeiro, usamos a linearidade do limite para reduzir a complexidade do nosso problema.
> * Em seguida, calculamos a derivada da função $N^l e^{-N}$. Utilizando desigualdades, vemos que $f^{\prime}(x) \geqslant 0$ em $[0, l]$  e $f^{\prime}(x) \leqslant 0$ em $[l,+\infty)$.
> * Pelo resultado abaixo, vemos que $x=l$ é máximo global de $f$.
> * Assim, obtemos a constante necessária para limitar nossa função por uma sequência que vai para zero...

