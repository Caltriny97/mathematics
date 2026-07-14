Data Criada: 27/04/2026 às 13:30
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

# Introdução: Método de Newton

[[Método de Newton]]


# Limites

O exemplo acima é um caso particular de limite de uma sequência.

Na prática, nós calculamos a **velocidade de convergência** para provar que o limite de uma sequência é uma número específico. Isso não é a mesma coisa de provar que existe um $n_{0}$ tal que o erro é menor que um dado valor.

Mas só vamos ver isso em análise. Aqui em cálculo, vamos aprender a calcular a velocidade com a qual uma sequência se aproxima do seu limite.

> [!definicao]
> Uma **sequência** é ume função de $\mathbb{N}$ em $\mathbb{R}$. Em vez de usar a notação $f: \mathbb{N} \rightarrow \mathbb{R}$, é mais comum usar a notação $\left(x_n ; n \in \mathbb{N}\right)$ para enfatizar o caráter sequencial da sequência.

Sequência é simplesmente uma notação que inventou-se para uma classe particular de funções.

Ps. Os termos estão ordenados (um termo vem depois do outro), por isso usamos essa notação que lembra os vetores, onde a ordem importa. Numa função, os termos do domínio não tem que estar ordenados.

> [!definicao]
> Uma sequência $\left(x_n ; n \in \mathbb{N}\right)$ é dita **decrescente** se $x_{n+1} \leqslant x_n$ para todo $n \in \mathbb{N}$. A sequência $\left(x_n ; n \in \mathbb{N}\right)$ é dita **limitada inferiormente** se existir $a \in \mathbb{R}$ tal que $x_n \geqslant a$ para todo $n \in \mathbb{N}$.

No nosso exemplo do método de Newton, provamos que a sequência é decrescente e limitada inferiormente por $\sqrt{ 2 }$. Para essas sequências decrescentes limitadas inferiormente, nós vamos definir o limite.

> [!definicao]
> Seja $\left(x_n ; n \in \mathbb{N}\right)$ decrescente e limitada inferiormente. O limite de $\left(x_n ; n \in \mathbb{N}\right)$ é dado por
> $
> \lim_{ n \to \infty } x_{n} := \operatorname{inf}\{x_{n};\; n \in \mathbb{N}\}
> $

> [!obs]
> Podemos extrapolar isso para sequências crescentes e limitadas superiormente. Daí, o seu limites serão os respectivos supremos

Nós provamos no exemplo que $\sqrt{ 2 }$ é o maior número que é menor que todos os termos da sequência, i.e., o ínfimo. Pelo axioma dos números reais, isso está bem definido.

Um detalhe interessante é que a sequência é decrescente, mas não estritamente decrescente. Por isso um número pode repetir várias vezes e depois talvez continuar decrescendo. Quando usamos o parênteses em $\operatorname{inf}\{x_{n};\; n \in \mathbb{N}\}$, as repetições não são contadas e a ordem deixa de importar.

Esta definição é muito geral e não nos disse muito sobre como calcular limites e/ou provar que o limite é uma valor dado. É legal do ponto de vista teórico, mas não ajuda nada na prática.


> [!definicao]
> Dizemos que uma sequência $\left(x_n ; n \in \mathbb{N}\right)$ **converge** a $+\infty$ (ou diverge a $+\infty$ ) se dado $M \in \mathbb{N}$, existe $n_0 \in \mathbb{N}$ tal que $x_n \geqslant M$ para todo $m \geqslant n_0$.

Isso se chama [[Propriedade arquimediana]]. Todas as sequências que têm a mesma propriedade, vai para infinito.

Essa é a definição mais geral (é a definição do epsilon e delta para o caso de limite $+\infty$, mas o Milton vai usar outra definição um pouco mais simples:

> [!definicao]
> Dizemos que uma sequência crescente $\left(x_n ; n \in \mathbb{N}\right)$ **converge** a $+\infty$ se ela não for limitada superiormente.

A sequência dos números naturais converge a $+\infty$ porque ela não é limitada superiormente (é a propriedade arquimediana). Contraexemplo: a sequência $x_{n} = \frac{n}{n+1}$ é crescente, mas é limitada por $1$.


Exemplos de sequências que convergem a $+\infty$:
1. $x_{n}= n$
2. $x_{n}=2^{n}$
3. $x_{n}=n^{l}, \;l \in \mathbb{N}$
4. $x_{n}=a^{n};\;a>1$
5. $x_{n} = 2^{2^{n}-3}$
$x_{n}=n$ converge a $+ \infty$ pela propriedade arquimediana. Já $x_{n}=2^{n}$ e $x_{n}=n^{l}$ são sempre maiores que $n$ para todo $n \in \mathbb{N}$. Então, $n$ carrega para $+ \infty$ as sequências $2^{n}$ e $n^{l}$. 

Isso não é verdade para $x_{n}=a^{n}; \; a>1$, isto é, não é verdade que $a^{n}>n$ para todo $n$. Porque se $a=1.1$ por exemplo, demora um pouco para começar a crescer. Temos que ir para em torno de $n=10$ para essa desigualdade ser verdade de fato. 

Usamos para mostrar isso **indução generalizada**. Assim, chegaremos que $a^{n}>n$ a partir de um certo $n_{0}$. Então aí novamente $n$ carrega $a^{n}$ para $+ \infty$.

Por fim, a sequência $x_{n} = 2^{2^{n}-3}$ é o inverso do erro que calculamos no método de Newton. Ela em particular não é carregada por $n$, mas sim por $2^{n}$. Então $2^{n}$ carrega $2^{2^{n}-3}$ para $+ \infty$. Note então que, se nós conhecemos uma sequência que vai para $+ \infty$, se a gente compor com uma outra sequência que vai para $+ \infty$, então o resultado também vai para $+ \infty$.

O que a gente vai ver é que: sempre vai ter uma sequência que vai carregar a gente para $+ \infty$. E é assim que a gente vai provar limites em geral. É assim que se prova que uma sequência qualquer tem um determinado limite: achar uma velocidade de convergência. Os inversos das sequências listadas acima são todas **velocidades de convergência**.

O pessoal em geral fala que a velocidade em si é a sequência que vai a $+ \infty$ e o erro seria o inverso disso.

> [!resumo]
> * Usamos a definição geral de convergência para mostrar que a sequência é maior que dado $M$ a partir de certo $n_0$.
> * Para aplicar a definição particular, precisamos mostrar que a sequência é crescente e que não é limitada superiormente.
> 	* Para mostrar que não é limitada superiormente nesse caso, usamos indução para mostrar que a sequência é maior que $x_n=n$ ou qualquer outra sequência que sabemos que tende a infinito. 


Exemplos de sequências que não convergem a $+\infty$:
1. $x_{n}=1$
2. $x_{n}=a;\;a\in \mathbb{R}$
3. $x_{n}=\frac{n}{n+1}$
4. $x_{n}=1-a^{n}; \; a \in (0,1)$
Elas ainda são crescentes, mas não são limitadas.


Essa definição específica do Milton não engloba por exemplo a sequência $x_{n}= n+\cos(n)$ porque não é crescente. Por enquanto, é um mistério porque ele só está usando sequências crescentes. Vamos descobrir daqui a pouco.

Por enquanto, convergência é só uma definição. Convergir a $+\infty$ é simplesmente outra maneira de dizer que a sequência não é limitada.


# Definição prática de limite

Seguindo a definição do Milton, provar que uma sequência crescente vai ou não para infinito não é muito difícil. Por isso, usaremos esse raciocínio para definir limite duma maneira prática, i.e., é o jeito no qual provamos que o limite existe ou que ele tem um valor limitado, etc.

Para isso, vamos definir subsequência.

> [!definicao]
> Seja $\left(x_n ; n \in \mathbb{N}\right)$ uma sequência. Uma **subsequência** de ( $x_n ; n \in \mathbb{N}$ ) é a composição ( $x_{N(n)} ; n \in \mathbb{N}$ ), da sequência $\left(x_n ; n \in \mathbb{N}\right)$ com uma função $N: \mathbb{N} \rightarrow \mathbb{N}$ estritamente crescente.

O que isso faz na prática? Bom, uma subsequência é uma nova sequência que pega somente alguns termos da sequência original.

**Exemplo:** Seja $x_{n}:=\sqrt{ n }$ para todo $n \in \mathbb{N}$. As sequências $(y_{n};n\in \mathbb{N})$, $(z_{n};n\in \mathbb{N})$ dadas por
$$
y_{n}:=n, \quad \quad z_{n}:=n^{3/2}
$$
para todo $n \in \mathbb{N}$, são subsequências de $(x_{n};n\in \mathbb{N})$. No caso, $y_{n}$ é resultado da composição de $x_{n}$ com a função $N(n)=n^{2}$, enquanto $z_{n}$ é resultado da composição com $N(n)=n^{3}$.


Temos duas formas equivalentes de pensar numa subsequência: a primeira é a definição acima, que é a composição de uma função estritamente crescente de $\mathbb{N}$ com a minha sequência original. Ela deve ser **estritamente crescente** porque não podemos repetir termos.

Essa é a definição matemática, mas o que isso significa na prática? Nós pegamos só alguns termos da sequência original na ordem certa. Por isso, $N(n)$ deve ser estritamente crescente, senão poderíamos não pegar na ordem certa e acabar voltando para trás na sequência. Mas não se pode voltar para trás numa subsequência: a ordem tem que ser a original, só que nós vamos descartar alguns termos da sequência original. Esse conceito é muito importante em Análise.


Por que a gente introduz o conceito de subsequência? Porque temos um teorema...

> [!teorema] Teorema 1.
> Uma sequência $(x_{n};n\in \mathbb{N})$ crescente satisfaz
> $
> \lim_{ n \to \infty }x_{n}=+\infty
> $
> se, e somente se, existir uma subsequência $\left(x_{N(n)} ; n \in \mathbb{N}\right)$ de $\left(x_n ; n \in \mathbb{N}\right)$ tal que
> $
> x_{N(n)} \geqslant n
> $
> para todo $n \in \mathbb{N}$.

> [!demonstracao]-
> Ver nota de aula 10 do Milton. A ideia da parte "somente se" consiste em 
> * Definir o conjunto dos índices da sequência que são maiores que determinado $n$. Se a sequência fosse limitada, haveria algum $n$ para o qual $A_n$ seria vazio. Como ela é ilimitada, $A_n$ é não vazio.
> * Definir uma função $N_0:\mathbb{N} \rightarrow \mathbb{N}$ dada por $N_0(n) = \operatorname{inf}A_n$.
> * Verificar que essa função é crescente, i.e., $N_0(n+1) \geqslant N_0(n)$.
> * Verificar que, por construção de $A_n$, temos que $x_{N_0(n)} \geqslant n$ para todo $n$, logo $x_{N_0(n)}$ é a subsequência desejada (apenas uma ressalve para ser estritamente crescente).
> * Na verdade, temos que definir $N(n):=N_0(n)+n$ para que a subsequência seja estritamente crescente (parte da definição de subsequência). Essa definição dá certo porque a soma de duas funções crescentes é crescente e, se ao menos uma delas for estritamente crescente, então a soma também é estritamente crescente.

Essa é nossa primeira definição de limite.

O que estamos fazendo aqui é partir do **Princípio Arquimediano** (a única coisa que estamos usando como axioma), i.e., a sequência $x_{n}=n$ converge a $+\infty$ porque ela não é limitada. Agora, o que o teorema nos diz é que qualquer sequência que converge a $+\infty$ é carregada para $+\infty$ pela sequência dos números naturais. 

> [!ps]-
> É claro que podemos ter sequências que crescem bem mais lentamente que $n$, mas o que o teorema nos diz é que sempre podemos pegar termos específicos (se ela for crescente e limitada) tais que formem uma subsequência da sequência original.
> 
> Como nós podemos pegar esses termos tão espaçados quanto queiramos, nós sempre (respeitando a hipótese) vamos conseguir uma subsequência que converge pelo menos tão rápido quanto $x_n=n$.

É por isso que é importante que a sequência seja crescente, porque se tomássemos só alguns termos da sequência e analisássemos só esses termos, não poderíamos deduzir nada sobre os termos do meio. Mas, como ela é crescente, nós podemos obter informação sobre o comportamento dela a partir de subsequências. Em particular, sabemos se ela vai para $+\infty$ ou não só olhando a subsequência.

> [!exemplo]- Contraexemplo.
> Mas afinal, mesmo que a sequência oscilasse, existir uma subsequência que vai para $+\infty$ não é informação suficiente para garantir que a sequência original converge a $+\infty$? Por que devemos exigir que ela seja crecente então?
> 
> A resposta é não! Se a sequência original puder oscilar livremente, o fato de existir uma subsequência que vai para $+\infty$ **não** garante que a sequência original inteira vá para $+\infty$. Veja o contraexemplo:
> 
> Imagine uma sequência $x_n$ definida da seguinte forma para cada termo $n$:
> 
> - Se $n$ for **par**: $x_n = n$
>     
> - Se $n$ for **ímpar**: $x_n = 0$
>     
> 
> Os primeiros termos dessa sequência são:
> 
> $(0, 2, 0, 4, 0, 6, 0, 8, 0, 10, \dots)$
> 
> ### 1. Olhando para a Subsequência Dos Pares:
> 
> Se escolhermos a subsequência dos termos pares, ou seja, $N(n) = 2n$, teremos:
> 
> $x_{N(n)} = x_{2n} = 2n$
> 
> Note que $2n \geqslant n$ para todo $n \in \mathbb{N}$. Essa subsequência cresce muito rápido e diverge para $+\infty$:
> 
> $\lim_{n \to \infty} x_{N(n)} = +\infty$
> 
> ### 2. O Comportamento da Sequência Original:
> 
> Olhando para a sequência inteira $x_n$, ela vai para mais infinito? **Não.** Por mais que ela atinja valores gigantescos nos números pares, ela sempre "desaba" de volta para zero logo em seguida, no número ímpar subsequente.
> 
> Para que $\lim_{n \to \infty} x_n = +\infty$, todos os termos (a partir de um certo ponto) precisam ser maiores do que qualquer número grande que você escolher (**essa é a definição mais geral que o Milton não quis usar**). Como os termos ímpares são sempre $0$, a sequência original não converge para $+\infty$; ela simplesmente **oscila e diverge**.
> 
> 

Esse teorema é muito útil para provar na prática que **sequências crescentes dadas convergem** para $+\infty$. A única coisa que temos que provar é que existe uma subsequência que cresce mais rápido que $n$, i.e., que vá pra $+\infty$ pelo menos com $n$ (outras podem convergir mais rápido). Podemos fazer essas provas por indução.

> [!obs]
> Podemos também aproveitar esse conceito de subsequência de outra forma... 
> * Uma dada sequência converge se, e somente se, todas as suas subsequências convergem para o mesmo valor
> 
> Acontece que não é muito prático usar esse resultado. Por isso mesmo condicionamos nossa definição ao caso de sequências estritamente crescentes. Porém, se usarmos sua contrapositiva, temos um resultado interessante:
> * Se uma sequência não converge, então existe pelo menos uma subsequência não convergente... (ver relação com o [[Teorema de Bolzano-Weierstrass]])


## Convergência para zero

> [!definicao]
> Dizemos que uma sequência $(x_{n};n\in \mathbb{N})$ **decrescente** de números **positivos** converge a $0$ se
> $
> \lim_{ n \to \infty } \frac{1}{x_{n}} = +\infty
> $
> Em outras palavras,
> $
> \lim_{ n \to \infty } x_{n} = 0 \iff \lim_{ n \to \infty } \frac{1}{x_{n}} = +\infty
> $

Para que essa definição faça sentido, $x_{n}$ deve ser **decrescente** (para que $\frac{1}{x_{n}}$ seja crescente). Além disso, $x_{n}$ deve ser **estritamente positiva**, senão, ao pegar o inverso, ou estaríamos dividindo por um número negativo, o que quebraria a lógica de $\frac{1}{x_{n}}$ ser crescente, ou estaríamos dividindo por zero.

Vamos ver agora o que o teorema que enunciamos anteriormente nos diz sobre limites para zero:

> [!teorema] Teorema 2.
> Seja $(x_{n};n\in \mathbb{N})$ uma sequência **decrescente**. Logo,
> $
> \lim_{ n \to \infty } x_{n} = 0
> $
> se, e somente se, existir subsequência $(x_{N(n)};n\in \mathbb{N})$ tal que
> $
> x_{N(n)} \leqslant \frac{1}{n}
> $

Na verdade, nós não precisamos usar $\frac{1}{n}$, mas sim qualquer sequência da nossa preferência que vá para zero (o inverso daquelas velocidades de convergências que vimos na 1ª parte da aula que convergem a $+\infty$ são alguns exemplos).

Todas as sequências que a gente já provou que convergem para $+\infty$ automaticamente nos dão sequências que convergem para $0$.

Esse teorema é consequência direta do teorema que estudamos acima que usa o princípio arquimediano. 


Agora, vamos generalizar a **definição de convergência para zero** para sequências **não negativas** (ambas estão muito relacionadas com o teorema do confronto). Essa definição que vamos ver não exige mais que a sequência seja decrescente, i.e., pode ser até mesmo oscilante.

> [!definicao] Convergência para zero.
> Dizemos que uma sequência $\left(x_n ; n \in \mathbb{N}\right)$ de números não negativos converge a $0$ se existir uma sequência $\left(y_n ; n \in \mathbb{N}\right)$ decrescente, de números positivos, convergente a $0$, tal que
> $x_n \leqslant y_n \;\;\text{para todo}\; n \in \mathbb{N}.$

Essa é a definição de convergência para zero. Então, o Milton toma o teorema do sanduíche como definição. Essa definição é exatamente o que fazemos na prática. Ele faz um breve resumo na aula 11 (lá ele fala que essa definição vale para qualquer sequência $x_{n}$ negativa ou não).


> [!resumo]
> * $\lim_{ n \to \infty }x_{n}=0$ se existir sequência decrescente $(z_{n};n \in \mathbb{N})$ tal que $|x_{n}| \leqslant z_{n} \; \; \forall n$ e
> $
> \lim_{ n \to \infty } z_{n}=0
> $
> * $\lim_{ n \to \infty }z_{n}=0$ se existir subsequência tal que
> $
> z_{N(n)} \leqslant \frac{1}{n} \quad \forall n \in \mathbb{N}
> $


# Definição de Limite

> [!definicao]
> Dizemos que uma sequência $\left(x_n ; n \in \mathbb{N}\right)$ **converge** a um número $x \in \mathbb{R}$ se a sequência $\left(|x_n-x| ; n \in \mathbb{N}\right)$ converge a $0$.


> [!obs]
> Repare que chegamos na definição de limite para um sequência qualquer (monótona, oscilatória, não importa!).
> 
> O ponto é que o Milton foi construindo o terreno até aqui usando sequências monótonas nas definições, o que me dava a impressão de perda de generalidade. 
> 
> Porém, na definição de convergência para zero, ele extrapolou as definições até então para sequências genéricas usando o teorema do sanduíche. Isso é o que nos permitiu agora generalizar para qualquer sequência.

Ver exemplos na minha nota de aula 10.01


# Propriedades dos limites

[[Propriedades dos limites]]

# Continuidade

* [[Continuidade]]

* [[Teorema do Valor Intermediário]]
* [[Teorema do Valor Extremo]]
* [[O primeiro teorema do valor médio (integrais)]]
* [[Teorema de Bolzano-Weierstrass]]