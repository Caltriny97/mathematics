Data Criada: 09/04/2026 às 17:40
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

> [!definicao]
> Uma matriz quadrada $A_{n \times n}$ é dita invertível (ou não singular) se existe uma matriz $B_{n \times n}$ tal que
> 
> $
> A B=I=B A .
> $
> 
> 
> Neste caso, a matriz $B$ é chamada de inversa de $A$ é denotada por $A^{-1}$.

> [!obs]
> Nos números reais, nós só podemos falar em inverso de $a$ se $a \neq 0$:
> $
> a x=b \quad \xrightarrow{a \neq 0} \quad x=a^{-1} b
> $
> No caso de matrizes, porém, não basta a matriz $A$ ser não-nula para ela ser invertível. Em outras palavras, existem matrizes não invertíveis (singulares) diferentes da matriz nula. Ainda vamos analisar essas condições...
> $
> A X=B \quad \xrightarrow{?} \quad X=A^{-1} B
> $
> Inclusive, essa é justamente a motivação para trabalharmos com matrizes inversas: achar soluções para [[Sistemas Lineares]]

Existe uma abordagem diferente, em que definimos a matriz inversa pela esquerda e pela direita. Ela é utilizada para estender nosso escopo para matrizes não quadradas. Por enquanto, vamos usar essa definição do slide, porque só estamos interessados nas matrizes quadradas mesmo. Pro nosso caso, teoricamente, precisamos verificar as contas da inversa pelos dois lados para mostrar que ela existe. Na sessão mais adiante, vamos ver um teorema que mostra não ser necessário para matrizes quadradas.


> [!teorema] Teorema 1.
> 1. Se a matriz $A_{n \times n}$ é invertível, então sua inversa é única.
> 2. Se a matriz $A_{n \times n}$ é invertível, então a matriz $A^{-1}$ também é invertível e $\left(A^{-1}\right)^{-1}=A$.
> 3. Se a matriz $A_{n \times n}$ e $B_{n \times n}$ são invertíveis, então a matriz $A B$ também é invertível e $(A B)^{-1}=B^{-1} A^{-1}$.
> 4. Se a matriz $A_{n \times n}$ é invertível, então a matriz $A^T$ também é invertível e $\left(A^T\right)^{-1}=\left(A^{-1}\right)^T$.

> [!demonstracao]- Demonstração e comentários.
> Ver demonstrações no slide 7.
> 
> **(i)** Quando queremos mostrar unicidade, supomos que os elementos são diferentes e mostramos a igualdade.
> 
> **(ii)** Observe que, nesses tipos de demonstrações em que queremos verificar certa propriedade, podemos simplesmente fazer o "caminho inverso": partir de onde queremos chegar e desenvolver até o ponto de início teórico. No caso das propriedades $3$ e $4$, teríamos:
> 
> ($3$) Queremos chegar que $(AB)(B^{-1}A^{-1})=I$. Ao invés de partir de $I$ e tentar chegar na igualdade, vamos desenvolver num rascunho o lado esquerdo e, na demonstração, apresentamos o contrário:
> $
> \text{rascunho:} \quad (AB)(B^{-1}A^{-1})=(AI)A^{-1}=AA^{-1}=I
> $
> Assim provamos de uma vez a existência do inverso e que ele é igual a $(B^{-1}A^{-1})$. Repare que não faz sentido nenhum nós fazermos esse desenvolvimento para a expressão $(AB)(AB)^{-1}$, pois isso é verdade por def. O que fizemos acima foi mostrar na verdade a equivalência entre $(AB)^{-1}$ e $B^{-1}A^{-1}$.
> 
> ($4$) Algo parecido acontece para a proposição $4$:
> $
> \text{rascunho:} \quad (A^{-1})^{t}(A^{t}) = (AA^{-1})^{t}=I^{t}=I
> $
> Nesse caso, uma outra solução poderia ser:
> $
> AA^{-1}=I \implies (AA^{-1})^{t}=I^{t} \implies (A^{-1})^{t}A^{t} = I
> $
> 
> 
> Outro ponto: Esses expoentes de $A^{t}$ e $A^{-1}$ são simplesmente **notações**. Nada tem a ver com expoentes ou algo relacionado. Só é conveniente e intuitivo para nós usar essas representações. Poderíamos denotá-los de modo completamente diferente, tipo um coração em volta da matriz (ver minha anotação).

> [!obs]
> Se as matrizes fossem inversas só por um lado, só uma dessas $3$ propriedades seria válida (precisamos verificar as ordens de cada multiplicação).


> [!teorema]
> Sejam $A$ e $B$ matrizes de ordem $n \times n$. Nestas condições:
> 
> $
> A . B=I \Leftrightarrow B . A=I .
> $
> 
> A prova deste teorema pode ser vista na videoaula sobre Matrizes Elementares - https://www.youtube.com/watch?v=Rnmeq5geMIw

Veja nas minhas notas da Unesp como conseguimos trocar realizar operações elementares nas matrizes com multiplicação entre matriz e outra matriz elementar correspondente.


# Cálculo da Matriz Inversa

Ver exemplo do slide e da minha anotação.

Lá, descrevemos a relação $AB = I$ (um simples produto matricial) por um [[Sistemas Lineares|sistema linear]] $4\times 4$, onde as variáveis são as entradas da matriz inversa $B$ e, vendo que as variáveis se repetem em pares de eq., conseguimos separá-lo em dois sistemas $2\times 2$. (sim, nós **começamos essa nota falando de matriz inversa para resolver SL** e agora, **para achar a inversa, precisamos resolver um SL**)

Daí, é só fazer o que já sabemos: escalonar os dois SL até atingir a identidade. O que ficar do lado direito das matrizes aumentadas são os valores das entradas da matriz inversa.

Só isso já estaria bom o suficiente, mas ainda temos mais uma carta: os coeficientes das nossas incógnitas (os termos da inversa) são os mesmos em ambos os sistemas $2 \times 2$, pelo que o lado esquerdo das matrizes aumentadas é o mesmo nas duas. Opa, então as operações elementares que resolvemos em ambas são as mesmas também. 

Então podemos adotar uma matriz aumentada maior ainda $[A|R|R^{'}]$, onde $[R|R^{'}]$ são os lados direitos das duas matrizes aumentadas antigas, que formam justamente os termos da matriz identidade. Assim, ao escalonarmos $A$, teremos do lado direito a matriz inversa completa para nós.

Um detalhe interessante é que, voltando pro sistema linear $4\times 4$ original, que mapeava as entradas da inversa, poderíamos escaloná-lo ali mesmo. Chegaríamos também na matriz identidade $I_{4}$, onde o lado direito seriam as soluções para as entradas uma a uma da inversa $B$.


**Sintetizando...**
$$
[A \mid I] \xrightarrow{\text { Escalonar }}[R \mid S] \rightarrow \begin{cases}R=I & \Rightarrow A \text { é invertível e } A^{-1}=S \\ R \neq I & \Rightarrow A \text { não é invertível }\end{cases}
$$
Isso acontece, pois o nosso candidato a matriz inversa $S$ deve possuir **solução única** (afinal, **a inversa é única**). E, para possui única solução, $R$ deve ser identidade. Qualquer outra coisa que aparecesse significaria que ou não tem solução ou infinitas soluções (veja análise das soluções em [[Sistemas Lineares]]).


> [!teorema]
> Seja $A_{n \times n}$ uma matriz quadrada. A é invertível se, e somente se, $A$ é equivalente por linhas à matriz identidade $I_n$.

Esse teorema é que formaliza tudo o que fizemos, usando multiplicação de matrizes elementares, mas não vamos fazer aqui. Ver minhas notas da Unesp.


Veja relação entre [[Matriz inversa e o SL]].


# Conjunto das Matrizes invertíveis

Fixado um $n \in \mathbb{N}_{>0}$, o conjunto das matrizes de ordem $n \times n$, invertíveis, com as operações usuais de matrizes, é um Espaço Vetorial?

Não, pois não é fechado para soma nem para o produto por escalar. Ver demonstração em [[Espaços Vetoriais e Subespaços Vetoriais]].


