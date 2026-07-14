Data Criada: 23/05/2026 às 20:24
Tags:

Provado por:
Referências:
Justificativas:

Especializações:
Generalizações:

# Declaração e Provas

> [!teorema]
> Sejam $a, b \in \mathbb{R}$ tais que $a<b$ e seja $\left(x_{n ;} ; n \in \mathbb{N}\right)$ sequência em $[a, b]$. Existe subsequência $\left(x_{N(n)} ; n \in \mathbb{N}\right)$ convergente.

Ex.: é fácil desenhar uma sequência que não é convergente, por exemplo: $x_{n}$ é igual a $a$ nos ímpares e igual a $b$ nos pares. Ela não converge, mas tem duas subsequências que convergem para limites diferentes.

> [!demonstracao]
> Ideia da prova: O método da biseção funciona aqui também. Basta escolher $I_{n+1}=A_n$ se a sequência tiver um número infinito de pontos em $A_{n}$ e $I_{n+1}=B_n$ senão.
> 
> Rever ideia no final da aula 13.

Na realidade, a linha de raciocínio é: prova-se o teorema de Bolzano-Weierstrass e a partir dele, prova-se o teorema do valor intermediário e o teorema do valor extremo. O que acontece é que são todos equivalentes, ou melhor, todos têm uma ideia principal: o método da bisseção. A partir dele, provamos os 3 teoremas. O mais interessante é que ele é fácil de ser aplicado computacionalmente.