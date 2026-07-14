Data Criada: 12/04/2026 às 21:40
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

# Funções monótonas

As funções podem ser:
* **Monótonas** quando a função é crescente ou estritamente crescente
* **Estritamente monótonas** quando a função é estritamente crescente ou estritamente decrescente.
* **Monótonas por partes**, num intervalo, se o gráfico é formado por um número finito de partes monótonas (as funções em escada são um exemplo).


# Integrabilidade de funções monótonas limitadas

Uma vez definido o que é a integral, vamos começar a analisar quais tipos de funções são de fato integráveis e, quando o forem, como podemos calcular...

> [!teorema]
> Se $f$ é monótona no intervalo fechado $[a,b]$, então $f$ é integrável em $[a,b]$.

A demonstração consiste em mostrar que $\bar{I} = \underline{I}$. No livro, isso é feito de modo análogo ao que fizemos em [[Método da Exaustão]] e na [[Aula 3.1  A Integral.pdf|nota de aula]] da monitoria (separando em intervalos $\frac{1}{n}$ iguais...), só que usando o conceito de funções em escada e partições (os intervalos $x_{k}-x_{k-1}$ não são iguais a $\frac{1}{n}$ necessariamente). Ele usou também a [[Soma Telescópica]]:
$$
\begin{aligned}
\int_a^b t_n-\int_a^b s_n & =\sum_{k=1}^n f\left(x_k\right)\left(x_k-x_{k-1}\right)-\sum_{k=1}^n f\left(x_{k-1}\right)\left(x_k-x_{k-1}\right) \\
& =\frac{b-a}{n} \sum_{k=1}^n\left[f\left(x_k\right)-f\left(x_{k-1}\right)\right]=\frac{(b-a)[f(b)-f(a)]}{n},
\end{aligned}
$$

Ver aula 4 do Milton:
![[Pasted image 20260412203854.png]]

![[Pasted image 20260412204043.png]]


# Cálculo da integral de uma função monótona limitada

> [!teorema]
> Seja $f$ crescente no intervalo fechado $\lfloor a, b\rfloor e x_k=a+k(b-a) / n$ para $k=0,1,2, \ldots, n$. Se I é qualquer número que verifica as desigualdades
> 
> $
> \frac{b-a}{n} \sum_{k=0}^{n-1} f\left(x_k\right) \leq I \leq \frac{b-a}{n} \sum_{k=1}^n f\left(x_k\right)
> $
> 
> para todo o inteiro $n \geq 1$, então $I=\int_a^b f(x) d x$.


