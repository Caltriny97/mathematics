Data Criada: 23/05/2026 às 12:49
Tags:

Provado por: [[Continuidade]], [[Limites]]
Referências:
Justificativas:

Especializações:
Generalizações:

# Declaração e Provas

> [!teorema]
> Seja $f:[a, b]$ contínua. Para todo $c$ entre $f(a)$ e $f(b)$ existe $x_* \in[a, b]$ tal que $f\left(x_*\right)=c$.

Em outras palavras, esse teorema nos diz que um função contínua para ir de um valor $a$ até $b$ deve passar por todos os valores entre $a$ e $b$.

Funções contínuas são sempre definidas em intervalos fechados.

![[Pasted image 20260523125704.jpg|center|400]]


> [!demonstracao]-
> A nota do Milton está um pouco diferente do que foi feito em sala na minha nota de aula 12.
> **1ª parte (simplificações)**
> * translação da função
> * Definição dos sinais
> * Mudança de escala
> Veja [[SPG]] para uma breve discussão sobre essa técnica. Na minha nota de aula 12, o Milton tomou SPG que $f(a) \leqslant f(b)$, porque temos $3$ casos possíveis: $f(a) \leqslant f(b)$, $f(a)=f(b)$ ou $f(a) \geqslant f(b)$. O segundo caso é trivial, pois $x_*=f(a)=f(b)$ e o terceiro caso é só provar tudo de forma análoga tomando a função auxiliar $g(x)=-f(x)$.
> 
> **2ª parte (método da bisseção)**
> Começamos com as barreiras $a_1=0$ e $b_1=1$. Olhamos para o ponto médio. 
> - Se a função for **negativa ou zero** no ponto médio, a barreira da esquerda ($a_{n+1}$) avança até o meio.
> - Se a função for **positiva** no ponto médio, a barreira da direita ($b_{n+1}$) recua até o meio.
>   
> **3ª parte (monotonicidade + continuidade)**
> Usando as primieras definições de limite com supremo e ínfimo, vemos que as sequências $a_n$ e $b_n$ convergem pro mesmo ponto. Agora que sabemos que as duas sequências espremeram o domínio até um único ponto $x_*$, olhamos para o que acontece com o valor da função ali:
> - Por construção, todos os pontos da sequência $a_n$ tinham valores de função menores ou iguais a zero ($f(a_n) \le 0$).
> - Pelo **Teorema da Monotonicidade** que ele provou na página 2 (se todos os termos de uma sequência são $\le 0$, o limite também tem que ser $\le 0$) , e usando o fato de que a função é contínua:
>     
>     $f(x_*) = \lim_{n\rightarrow\infty} f(a_n) \le 0$
> - Por outro lado, todos os pontos da sequência $b_n$ tinham valores de função maiores que zero ($f(b_n) > 0$). Usando a mesma lógica do limite:
>     
>     $f(x_*) = \lim_{n\rightarrow\infty} f(b_n) \ge 0$
> 
> Isso tudo é muito fácil de se implementar algoritmicamente: um método de busca baseado no método da bisseção (relação com árvore binária). Ver a demonstração do Milton na minha nota de aula [[Teorema do Valor Intermediário.pdf]].


