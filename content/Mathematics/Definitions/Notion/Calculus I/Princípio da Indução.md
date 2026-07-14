Data Criada: 22/03/2026 às 18:26
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

> [!axioma] Axioma (Princípio de Indução).
> Seja $A$ um subconjunto de $\mathbb{N}$ satisfazendo as duas propriedades abaixo:
> (a) $1 \in A$.
> (b) Se $n \in A$, então $n+1 \in A$.
> 
> Logo, $A=\mathbb{N}$.

O Princípio de Indução é um dos Axiomas de Peano a respeito dos números naturais (será visto em curso de Análise na Reta). Ver anotações da aula 1.2 para uma breve introdução ao tópico.

> [!comentario]
> Na aula 3 do Milton, a definição foi um pouco diferente:
> 	Seja $S \subseteq R$ tal que
> 	(a) $1 \in S$.
> 	(b) Se $x \in S$, então $x+1 \in S$.
> 	Temos que $\mathbb{N} \subseteq S$.
> Note que ele não colocou $\mathbb{N} = S$, pois pode ser que $1,5$ por exemplo está em $S$ por algum motivo.

> [!comentario]
> No livro do apostol e na aula 1.2, esse princípio foi enunciado como um teorema, que pode ser provado pelos axiomas dos números reais. Mas não vamos entrar nessa questão.

> [!problema]
> Como usamos o axioma acima? Digamos que queremos provar uma certa afirmação, a qual depende de $n \in \mathbb{N}$. Por exemplo, digamos que queremos mostrar que $2^n>n$ para todo $n \in \mathbb{N}$. Seja $A$ o conjunto dos naturais para os quais esta afirmação é válida, ou seja, $A = \{n \in \mathbb{N}; 2^{n}>n\}$. Temos que
> 
> (a) Como $2^1=2>1$, concluímos que $1 \in A$.
> (b) Seja $n \in A$. Então $2^n>n$. Multiplicando esta inequação por 2, obtemos $2^{n+1}>2 n=n+n \geq n+1$ (sabemos que $n>1$ pela def. dos naturais). Ou seja, $n+1 \in A$.
> 
> Daí, pelo Princípio de Indução, $A=\mathbb{N}$.


> [!resumo] Plano Geral para Soluções pelo Método de Indução Matemática.
> 
> 
> 1. 
>    * (i) Encontre, no enunciado do problema, uma série de proposições semelhantes. Se as variáveis estiverem escondidas, você deve explicitá-las reformulando o problema. Se não existe uma cadeia, invente uma para que o problema se o problema seja parte dela.
> 
> 	* (ii) Se tivermos uma cadeia de perguntas em vez de uma cadeia de afirmações em um problema matemático, insira respostas hipotéticas. Você pode adivinhar as respostas experi- mentando com as primeiras perguntas na cadeia. Entretanto, depois que você tiver certeza de stas não se que as respostas estao corretas, não se esqueça de prová-las rigorosamente.
> 
> 3. Prove a primeira proposição (**passo básico**).
> 4. Prove que, qualquer que seja o número natural $n$, a veracidade da $n$-ésima proposição implica a veracidade da ($n+1$)-ésima proposição (**passo indutivo**). 
> 5. Uma vez demonstrados os passos básico e indutivo, todas as proposições na série estão demonstradas simultaneamente, já que é possível chegar a qualquer uma delas a partir da base "passo a passo".

> [!ps]
> Tirado do diálogo do livro "Círculos Matemáticos: a experiência Russa". Ver o problema dos quadrados e o problema das retas.


**Minha análise.**
(...)


> [!problema]-
> **Problema:** Em quantas partes $n$ retas dividem um plano se duas delas nunca são paralelas e três delas nunca se encontram no mesmo ponto?
> 
> Primeiro, vamos visualizar o problema para $n$ pequenos. Seguindo o passo 1.i, chegaremos a uma resposta hipotética, ou seja, uma conjectura: $L_{n}=1+(1+2+\dots+n)$. Agora vamos demonstrá-la formalmente:
> 
> **Passo básico:** Verifique $P(1)$
> **Passo Indutivo:** Assumindo como hipótese a nossa conjectura para $n$ retas, vamos "esquecer" essa conjectura e abstrair nosso problema para $n$ retas. Depois vamos tentar conceber como a adição da $(n+1)$-ésima reta interferiria no nosso $L_{n}$ e, por fim, vamos ver se a nossa fórmula "acompanha" essa transição de $n$ para $n+1$.
> 
> Imagine que já temos $n$ retas no plano. Ao adicionar a $n$-ésima reta, ela deve cruzar todas as $n$ retas anteriores (pois nenhuma é paralela) em pontos diferentes (pois não há três retas concorrentes).
> 
> Ao cruzar $n$ retas, a nova reta é dividida em $n+1$ segmentos. Cada um desses segmentos atravessa uma região já existente e a divide em duas. Portanto, adicionar a $n+1$-ésima reta adiciona exatamente $n+1$ novas regiões ao plano.
> $
> R_{n+1}=R_{n}+(n+1)
> $
> Manipulando algebricamente e usando soma telescópica, chagamos que:
> $
> R_{n+1}=\frac{n^{2}+3n+4}{2}
> $
> Acontece que isso é exatamente a fórmula original (nossa hipótese) trocando $n$ por $n+1$. Portanto, a nossa prova está completa.


> [!axioma] Axioma (Variante do Princípio de Indução).
> Seja $A \subset \mathbb{N}$ satisfazendo as duas propriedades abaixo:
> (a) $k \in A$,
> (b) Se $n \in A$, então $n+1 \in A$.
> 
> Então $A \supset\{k, k+1, k+2, k+3, \ldots\}$.


> [!axioma] Axioma (Princípio de Indução Generalizado ou Forte).
> Seja $A \subset \mathbb{N}$ satisfazendo as duas propriedades abaixo:
> (a) $\{k,\dots,k+l\} \subset A$,
> (b) Para todo $n\geq l$, vale que: se $\{k, \ldots, k+n\} \subset A$, então $k+n+1 \in A$.
> 
> Então $A \supset\{k, k+1, k+2, k+3, \ldots\}$.

> [!comentario]
> Essa variante é útil para provar por exemplo: mostre que os termos múltiplos de 3 da sequência de Fibonacci são pares. As outras variantes da indução não serviriam pra provar esse resultado, uma vez que ele depende de termos anteriores a $n$. Com essa variante generalizada, podemos tomar como válidos todos os termos antes de $n$ e, satisfazendo (a) e (b), generalizar para $\{k, k+1, \dots\}$. Ver detalhes na nota de aula 2.


> [!problema]
> Prove que todo $n \geq 2$ natural é primo ou pode ser escrito como produto de números primos.
> 
> **Solução:** Como $n=2$ é primo, temos a base de indução. Suponha que o resultado seja válido para quaisquer naturais no conjunto $A = \{2,3 \ldots, n-1,n\}$, que é a chamada hipótese de indução. Considere o natural $n+1$. Se $n+1$ é primo, temos o que se deseja provar, ou seja, $n \in A$. Se $n+1$ não é primo, então é produto de dois naturais $x$ e $y$, sendo $2 \leq x \leq n$ e $2 \leq y \leq n$. Pela hipótese de indução, $x$ e $y$ são produtos de números primos e, por conseguinte, $n+1=x \cdot y$ também é produto de números primos e, portanto, $n+1 \in A$. Portanto, pelo Princípio de Indução Generalizado, todo natural $n \geq 2$ é primo ou é um produto de primos.
> 
> 
> Um comentário importante: indução é um método de prova. Para buscar o enunciado correto a ser provado, é necessário buscá-lo por outros meios, tal como testes com valores pequenos de $n$ e buscar um padrão que leve a uma conjectura; "chutar" que a fórmula buscada é de um certo tipo (polinomial, exponencial etc.) e usar valores baixos de $n$ para encontrar as constantes na fórmula; ou usar outras ferramentas matemáticas. Um roteiro para realizar provas por indução seria:

> [!resumo] Roteiro.
> (1) Obtenha a base da indução, ou seja, mostre que a afiramação é correta para um certo natural $n_{0}$. Se for necessário usar indução forte, a base de indução pode ser composta por mais de um elemento.
> (2) Suponha que o resultado seja válido para um certo $n$ (ou para $n_{0},\dots,n$ no caso de indução forte), que é a chamada hipótese de indução.
> (3) Assumindo a hipótese de indução, mostre que a afirmação correspondente a $n+1$ é verdadeira.
> (4) Conclua, usando o Princípio de Indução, que a afirmação é válida para todo $n\geq n_{0}$.


# Paradoxo dos cavalos

> [!problema]-
> **Exercício 1.1.17.** Vamos provar o seguinte teorema: "Se numa sala com n pessoas há pelo menos um torcedor do Fluminense de Feira, então todos são torcedores do Fluminense de Feira".
> 
> **Demonstração:** por indução. Para $n=1$, só há uma pessoa na sala, então esta pessoa é torcedora do Fluminense de Feira.
> 
> Suponha o resultado válido para um certo $n \in \mathbb{N}$. Considere então uma sala com $n+1$ pessoas, onde pelo menos uma é torcedora, que chamaremos de pessoa $A$. Tire um pessoa $B$ da sala. Ficaram $n$ pessoas, incluindo a pessoa $A$. Pela hipótese de indução, essas $n$ são torcedoras. Tire uma pessoa qualquer da sala e coloque a pessoa $B$ que estava fora para dentro. Aplicando novamente a hipótese de indução para $n$, concluímos que a pessoa $B$ também é torcedora. Ou seja, todas as $n+1$ pessoas são torcedoras. Daí, pelo Princípio de Indução, concluímos que o resultado é válido para qualquer $n \geq 1$.
> 
> Bem, você deve ter desconfiado que esse teorema é falso. Encontre o erro na demonstração acima.
> 
> **Resposta.** Seja 
> $
> \{n \in \mathbb{N}; \text{se existem}\; n\; \text{pessoas numa sala com ao menos} \; 1 \; \text{torcedor}  \implies \text{todos são torcedores}\}$ 
> $
> O erro na demonstração não está na base da indução, mas sim no passo indutivo, especificamente na transição de $n=1$ para $n=2$. Observe o que acontece:
> 
> Suponha uma sala com 2 pessoas: $\{A,B\}$. Sabemos que pelo menos uma é torcedora: $A$. Quando nós vamos colocar o $B$ de volta e retiramos $A$, reta o conjunto $\{B\}$. O argumento afirma que, pela hipótese de indução, as pessoas nesse novo grupo de tamanho $n$ também devem ser torcedoras. Aqui está o erro:
> Para afirmar que $B$ é torcedor baseando-se no grupo anterior, o novo grupo precisaria contar alguém que já sabemos ser torcedor para validar a hipótese. No caso de $n=2$, os conjuntos $\{A\}$ e $\{B\}$ são disjuntos.
> 
> Isso tudo é verdade para $n\geq 2$, no entanto, como a lógica falha na transição de $n=1$ para $n=2$, a corrente da indução é quebrada logo no início e a afirmação geral se torna falsa. 
> 
> Podemos até pensar: e se forçarmos o nosso caso base para $n=3$? Acontece que aí se torna impossível provar o caso base. Para $n=1$, era óbvio que, se a sala tem $1$ pessoa e, ao menos $1$ é torcedora, então todas são. Agora, para $n=3$, se a sala têm $3$ pessoas e, ao menos $1$ é torcedora, é visível que a tese "todas são torcedoras" é falsa. Como a base é falsa, a fileira de dominós da indução nem começa a cair.
> 
> Esse problema é conhecido como o **Paradoxo dos Cavalos**.

**PS.** tirado do PCP


# Referências

* Princípio de Combinatória e Probabilidade - T. Franco
* Círculos Matemáticos: a experiência Russa