Data Criada: 30/05/2026 às 12:51
Tags:

Provado por:
Referências:
Justificativas:

Especializações:
Generalizações:

# Método de Newton

Como aproximar $\sqrt{ 2 }$ numericamente? Pelo Método de Newton:

A ideia aqui é: se $x$ é uma aproximação para $\sqrt{ 2 }$, então $$f(x) = \frac{1}{2}\left(x+\frac{2}{x}\right)$$ é uma aproximação melhor. Mas em que sentido essa sequência de aproximações têm como limite o tal de $\sqrt{ 2 }$. Para tanto, definimos $x_{n}$ de maneira recursiva. $$
x_{n} = f(x_{n-1})
$$Definir de forma recursiva torna prática a demonstração de propriedades da sequência a posteriori: usando, por exemplo, indução.

Mas como podemos saber a velocidade de convergência? Em outras palavras, qual é o erro que estamos cometendo? Para isso, provaremos algumas propriedades por indução:


* a) Para todo $n \in \mathbb{N}$, $x_{n}^{2}>2$
Isso é mais fácil que provar que $x_{n}>\sqrt{ 2 }$. 
BI: de fato, $x_{1}^{2}=4>2$. Vamos agora fazer um rascunho de trás para frente e depois escreveremos a prova resumida por indução:
$$
\begin{gather}
\text{Rascunho:} \\
\left(\frac{1}{2}\left(x+\frac{2}{x}\right)\right)^{2} \geq 2 \iff \frac{1}{4}\left(x+\frac{2}{x}\right)^{2}\geq 2 \iff x^{2}+4+\frac{4}{x^{2}}\geq 8 \iff x^{2}-4+\frac{4}{x^{2}}\geq 0 \iff \left(x-\frac{2}{x}\right)^{2}\geq 0\\
 \\
\text{Demonstração} \\
\left(x_n-\frac{2}{x_n}\right)^2>0 \Rightarrow x_n^2-4+\frac{4}{x_n^2}>0 \Rightarrow\left(x_n+\frac{2}{x_n}\right)^2>8 \Rightarrow 4 x_{n+1}^2>8 \Rightarrow x_{n+1}^2>2 .
\end{gather}
$$
Perceba que só podemos fazer essa "inversão", porque as passagens são se, e somente se.
<mark class="hltr-pink">Não daria pra fazer isso sem usar indução?</mark>

* b) Para todo $n \in \mathbb{N}$, $x_{n+1} < x_{n}$.
Vamos prová-la por indução. Primeiro, faremos um rascunho de trás pra frente (partindo da tese) e depois escreveremos a demonstração certinha partindo da hipótese: $x_{n}^{2}>2$.
$$
\begin{gather}
\text{Rascunho:} \\
\frac{1}{2}\left(x+\frac{2}{x}\right) \leq x \iff x +\frac{2}{x} \leq 2x \iff \frac{2}{x}\leq x \iff 2 \leq x^{2} \\
 \\
\text{Demonstração:} \\
x_n^2>2 \Rightarrow x_{n} > \frac{2}{x_n} \Rightarrow 2 x_n>x_n+\frac{2}{x_n} \Rightarrow x_n>\frac{1}{2}\left(x_n+\frac{2}{x_n}\right)=x_{n+1} .
\end{gather}
$$
Repare que nós só podemos fazer essa manobra porque as passagens do rascunho são se, e somente se (no caso, $x_{n}>0$ desde o começo, por isso podemos dividir as desigualdades) Isso é uma estratégia arriscada, principalmente com desigualdades.


Até agora, provamos que essa diferença $x_{n}^{2}-2$ é decrescente e maior que zero. Só que ainda não sabemos se a sequência converge exatamente para $\sqrt{ 2 }$. Em outras palavras, não sabemos se essa aproximação vai ficar arbitrariamente boa quando aumentamos $n$ (vai que a partir do $n=30$, a aproximação não melhora...).

Resumindo, a gente provou que a cada passo adicional, obtemos uma aproximação melhor. Mas ainda não provamos que essa aproximação é arbitrariamente boa. Para isso, temos que achar a **velocidade de convergência**, ou seja, uma estimativa da distância entre $x_{n}$ e $\sqrt{ 2 }$.


* c) Para todo $n \in \mathbb{N}$, $x_{n}^{2}-2\leq \frac{1}{2^{2^{n}-3}}$.
A ideia aqui é achar uma recorrência, ou seja, uma fórmula para essa diferença em função de termos anteriores. De fato, $x_{1}^{2}-2=2$, e
$$
\begin{gather}
x_{n+1}^{2}-2 = \left(\frac{1}{2}\left(x_{n}+\frac{2}{x_{n}}\right)\right)^2-2=\frac{1}{4} \cdot\left(\frac{x_{n}^2+2}{x_{n}}\right)^2-2= \\
 \\
\frac{\left(x_{n}^2+2\right)^2-8 x_{n}^2}{4 x_{n}^2}=\frac{\left(x_{n}^2-2\right)^2}{4 x_{n}^2} \leq \frac{(x_{n}^{2}-2)^{2}}{8}
\end{gather}
$$
pois $x_{n}^{2}>2$. Isso não é uma fórmula exata para essa diferença, por causa da desigualdade. É importante fazermos isso para tirar o $x_{n}$ do denominador, mesmo obtendo uma estimativa superior. O numerador está bom, pois está em função do termo anterior (recorrência).

Por enquanto essa desigualdade não provou nada. Ela é uma hipótese indutiva de algo que ainda nem sabemos o que é. Agora vamos descobrir exatamente quem é essa hipótese. Como descobrimos o que devemos colocar numa desigualdade para provar por indução? Nós fazemos alguns casos...
$$
\begin{gather}
x_{1}^{2}-2=2 \\
x_{2}^{2}-2\leq \frac{4}{8}=\frac{1}{2} \\
x_{3}^{2}- 2 \leq \frac{1}{4} \cdot \frac{1}{8} = \frac{1}{2^{5}} \\
x_{4}^{2}-2 \leq \frac{1}{2^{10}} \cdot \frac{1}{2^{3}} = \frac{1}{2^{13}} \\
x_{5}^{2}-2 \leq \frac{1}{2^{26}} \cdot \frac{1}{2^{3}} = \frac{1}{2^{29}} \\
\end{gather}
$$
Vamos tentar generalizar isso. Denotemos então
$$
\begin{gather}
x_{n+1}^{2}-2 \leq \frac{1}{2^{a(n+1)}}
\end{gather}
$$
Mas,
$$
a(n+1) = 2 \cdot a(n) +3
$$
Agora, vamos achar a solução dessa recorrência linear, i.e., achar uma expressão da forma $a(n)=2^{n}+b$:

Primeiro substituímos a expressão para $a(n+1)$ na desigualdade $x_{2}^{2}-2\leq \frac{1}{2}$ e achamos que $a(1)=-1$. Agora, podemos achar a solução:
$$
a(n) = 2^{n} -3 
$$

Agora sabemos nossa hipótese indutiva: queremos mostrar que para todo $n \in \mathbb{N}$,
$$
x_{n}^{2}-2\leq \frac{1}{2^{2^{n}-3}}
$$
De fato, $x_{1}^{2}-2=2$, logo a base da indução é válida. Agora, vamos supor que vale para $n$. Note que, pela desigualdade que obtivemos, temos
$$
x_{n+1}^{2} -2 \leq \frac{1}{2^{2^{n+1}-6}} \cdot \frac{1}{2^{3}} = \frac{1}{2^{2^{n+1}-3}}
$$
Logo, por indução, a desigualdade é válida.


* d) Em particular,
$$
x_n-\sqrt{2}=\frac{x_n^2-2}{x_n+\sqrt{2}} = x_n^2-2 \cdot \frac{1}{x_n+\sqrt{2}} \leqslant \frac{1}{2^{m}} \cdot \frac{1}{2 \sqrt{2}} \leqslant \frac{1}{2^{m+1}} \text {, onde } m=2^{n}-3
$$
Nós temos uma expressão para o erro $x_{n}^{2}-2$, mas nós queremos $x_{n}-\sqrt{ 2 }$. Depois, nós aplicamos uma cota inferior para $x_{n}$ no denominador para ter uma cota superior da fração $\frac{1}{x_{n}+\sqrt{ 2 }}$. Agora então, nós vamos aplicar a soma pela diferença para achar a desigualdade em termos de $\sqrt{ 2 }$.