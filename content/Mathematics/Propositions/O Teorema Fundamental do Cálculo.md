Data Criada: 06/06/2026 às 12:44
Tags:

Provado por: [[O primeiro teorema do valor médio (integrais)]]
Referências: [[Continuidade]], [[Derivadas]]
Justificativas:

Especializações:
Generalizações:

# Introdução

Derivada e integral são uma inversa da outra. Isso vai nos ajudar muito para calcular integrais. 

Numericamente, nós calculamos integrais por aproximações de retângulos, mas do ponto de vista teórico, usaremos TFC para calculá-las.


# Observação sobre os polinômios mônicos

> [!container] Contextualizando...
> Notemos que para $F(x)=x^n, \; n \in \mathbb{N}, \;\; F^{\prime}(x)=n x^{n-1}$ Por outra parte, para $n \in \mathbb{N}_0$,
> 
> $
> \int_a^b x^m d x=\frac{b^{m+1}-a^{m+1}}{m+1} .
> $
> 
> 
> Definindo $F(x)=x^n$ e $f(x)=n x^{n-1}$, vemos que
> 
> $
> \int_a^b f(x) d x=\int_a^b n x^{n-1} d x=b^n-a^n=F(b)-F(a),
> $
> 
> e que $F^{\prime}(x)=f(x)$. Por linearidade, a mesma fórmula vale para polinômios: seja $P: \mathbb{R} \rightarrow \mathbb{R}$ um polinômio e seja $p: \mathbb{R} \rightarrow \mathbb{R}$ dada por $p(x)=P^{\prime}(x)$ para todo $x \in \mathbb{R}$. Teremos que
> 
> $
> \int_a^b p(x) d x=P(b)-P(a)
> $
> 
> para todo $a, b \in \mathbb{R}$.
> 
> Esta fórmula vale **para toda** função contínua (relembre [[Continuidade]]), como o próximo teorema mostra:


# O Teorema Fundamental do Cálculo

> [!teorema]
> Seja $f:[a, b] \rightarrow \mathbb{R}$ contínua, e seja $F[a, b] \rightarrow \mathbb{R}$ dada por
> 
> $
> F(x):=\int_a^x f(y) d y
> $
> 
> para todo $x \in[a, b]$. Então $F$ é diferenciável para todo $x \in(a, b)$ e $F^{\prime}(x)=f(x)$.

> [!demonstracao]-
> Ver demonstração na nota de aula 19 do Milton e parte do desenvolvimento na minha nota de aula 19.
> * Começamos ao contrário: partimos de $f$ contínua e definimos $F$ a partir dela.
> * Utilizamos [[O primeiro teorema do valor médio]] para tal resultado.
> * Não supomos em momento nenhum que $F(x)$ é contínua. O TVM para integrais nos ajudou nisso.
> * Utilizamos a convenção dos sinais da integral para extrapolar para sequências $x_n$ quaisquer, a fim de calcular a derivada.
> 
> Resumindo a ideia: nós queremos mostrar que $F(x)$ é diferenciável. Como não há critério fácil para isso, pelo que vimos em [[Derivadas]], nós precisamos calcular explicitamente a o limite da derivada. Antes, nós vamos tentar simplificar a sequência dada por
> $
> \dfrac{F(x_n)-F(x)}{x_n-x}
> $
> Abrindo a expressão, nós chegamos num termo bem familiar: o termo do [[O primeiro teorema do valor médio (integrais)]]. Como $f$ é contínua por hipótese, podemos definir $y_n$ tal que $f(y_n)$ é igual ao termo acima. Agora, podemos usar o teorema do sanduíche para as distâncias $|y_n-x|$ e $|x_n-x|$ para mostrar que $y_n$ converge a $x$. Por continuidade da $f$, segue que $f(y_n) \rightarrow f(x)$.
> 
> Ou seja, nós tomamos a sequência $x_n$ convergente a $x$, mas ainda não sabemos se o termo acima converge. Agora, no entanto, nós acabamos de associar o termo acima com $f(y_n)$, que sabemos, por continuidade, que o limite existe e que é igual a $f(x)$, logo a derivada $F^{\prime}(x)$ existe e é igual a $f(x)$. 
> 
> <br>
> 
> Outra forma de provar isso seria mostrando que qualquer função contínua pode ser aproximada uniformemente por um polinômio interpolador de Lagrange. Como provamos o TFC para polinômios, podemos usar esse caminho para extrapolá-lo a qualquer função contínua.

Repare que o enunciado do TFC é mais forte do que apresentamos na sessão anterior. Lá, nós já sabíamos que $F(x)=x^{n}$ é diferenciável e que sua derivada é uma função contínua. O TFC nos garante que, se $f$ é contínua, a função $F(x)$ é diferenciável. Assim, a fórmula da sessão anterior é um corolário do TFC.


# Discussão sobre o $F(a)$ e a antiderivada

> [!corolario]
> Se escolhermos $x=b$, temos
> $
> \int_a^b f(x) d x= F(b)
> $

> [!obs]
> **A pergunta é: cadê o $F(a)$?**
> A fórmula enunciada na observação dos monômios tinha $F(a)$, mas a fórmula que provamos não a tem.
> 
> O que acontece é que, lá em cima, nós começamos supondo que a derivada $F^{\prime}(x)=f(x)$, mas essa função $F(x)$ **não** é unica, porque a derivada da função constante é zero.
> 
> Então, se adicionarmos uma constante à função $F(x)$, essa função ainda tem derivada igual à $f(x)$. Então, temos que escrever uma fórmula que leve em consideração essa possível constante.
> 
> O ponto é que: a função $F$ que definimos no teorema é igual a zero em $a$. Mas, se ela não fosse, teríamos que subtrair $F(a)$.


> [!definicao]
> Seja $f:[a, b] \rightarrow \mathbb{R}$ contínua. Uma **antideriveda** (ou **primitiva**) de $f^{\prime}$ é uma função $F:[a, b] \rightarrow \mathbb{R}$ diferenciável em $(a,b)$ tal que
> $
> F^{\prime}(x)=f(x)
> $
> para todo $x \in(a, b)$.

> [!proposicao]
> **a)** A função
> 
> $
> F(x):=\int_a^x f(y) d y
> $
> 
> é uma antiderivada de $f$.
> 
> <br>
> 
> **b)** Se $G$ for outra antiderivade de $f$, então
> 
> $
> F(x)=G(x)-G(a) .
> $
> 
> 
> Em particular,
> 
> $
> \int_a^b f(x) d x=G(b)-G(a)
> $

A resposta está aqui: toda antiderivada se diferencia da função $F(x)$ original enunciada em a) por uma constante.

> [!demonstracao]- Demonstração da parte b)
> A parte a) é corolário do TFC. Já a parte b) é mais delicada:
> Seja $H(x):=G(x)-F(x)$. Temos que $H^{\prime}(x)=0$ para todo $x \in(a, b)$ e $H$ é contínua em $[a, b]$. Seja $x \in (a, b]$. Pelo [[Teorema do Valor Médio|TVM]], eviste $y \in(a, x)$ tal que
> $
> \frac{H(x)-H(a)}{x-a}=H^{\prime}(y) .
> $
> mas $H^{\prime}(y)=0$. Portanto, $H(x)=H(a)$
> 
> O que o TVM está nos dizendo é que: toda função cuja derivada é igual a zero tem de ser constante. Isso implica que, dadas duas antiderivadas da mesma função, sua diferença é constante. Por fim, isso implica a fórmula enunciada na parte b), que é a fórmula mais conhecida do TFC.


# Aplicação

O teorema fundamental do cálculo é a principal ferramenta para calcular integrais, pois calcular derivadas é mais fácil. Em particular, qualquer fórmula de derivação nos dá una fórmula de integração. Poderiam ser provadas pela definição, porém são mais fáceis via TFC.

A regra da cadeia e a fórmula de Leibniz (relembre [[Propriedades da derivada]]) combinadas com o TFC nos dão duas fórmulas de integração muito importantes:
* [[Fórmula de integração por partes]]
* [[Fórmula de mudança de variáveis]]

Ver [[Notação de Leibniz]]

Entenda [[Integral definida & integral indefinida]].


