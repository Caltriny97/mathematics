Data Criada: 23/05/2026 às 20:53
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

# Introdução 

Vamos começar com um problema: calcular a reta tangente à parábola  definida por $f(x)=x^{2}-2$ de forma geométrica. Primeiro, precisamos de uma definição de reta tangente. Para começar, adotaremos a seguinte definição para o caso da **parábola**:

Uma reta $l(x)=ax+b$ é tangente ao gráfico de $f$ se a equação $f(x)=l(x)$ tem uma **única** solução.

Repare que nós excluímos a reta vertical nessa definição, pois ela não é descrita por uma função.

> [!container] 1ª abordagem.
> Nossa intenção aqui é partir de uma **regra genérica** para a reta tangente e ver que condições $a,b$ devem satisfazer para que haja somente um ponto de intersecção com a parábola.
> 
> Agora, nós igualamos a equação da reta tangente com a equação da parábola e teremos uma eq. do segundo grau. Como queremos uma única solução, igualamos a discriminante a zero e achamos uma relação entre $a$ e $b$. Resolvendo a equação, achamos $x_{0}$ em função de $a$. Temos $3$ eq. e $2$ incógnitas. Vamos colocá-las todas em função de uma variável livre: o $x_{0}$, que é a coordenada horizontal.
> 
> Por fim, chegamos na equação da reta tangente $l(x)=2x x_{0}-x_{0}^{2}-2$. A inclinação dessa reta é $a=2x_{0}$.


> [!obs]- Método de Newton.
> Notemos que a reta tangente parece intersectar o eixo $x$ perto de $\sqrt{2}$. De fato, ela intersecta o eixo $x$ em
> $
> \phi\left(x_0\right):=\frac{1}{2}\left(x_0+\frac{2}{x_0}\right) .
> $
> 
> A sequência $\left(x_n ; n \in \mathbb{N}_0\right)$ definida como $x_0=2$ e
> $
> x_n=\phi\left(x_{n-1}\right) \text { para todo } n \in \mathbb{N}
> $
> satisfaz
> $
> \lim _{n \rightarrow \infty} x_n=\sqrt{2},
> $
> 
> e a aproximação de $\sqrt{2}$ por $\left(x_{n}, n \in \mathbb{N}\right)$ é conhecida como método de Newton.
> 
> ![[Pasted image 20260523212223.jpg|center|400]]
> 
> 
> Então o método de Newton é um método muito geral para procurar zeros de funções $f$. Ele consiste em traçar a tangente num ponto dado à função $f$, olhar onde a reta tangente intersecta o eixo $x$ e adotar essa intersecção como $x_{n+1}$, isto é, como aproximação seguinte do zero. E assim sucessivamente.


> [!container] 2ª abordagem.
> O próximo passo é generalizar esse resultado para qualquer função quadrática $f(x)=ax^{2}+bx+c$. 
> 
> Para isso, usamos a fórmula **ponto-inclinação** para deixar a inclinação da reta em função de dois pontos $x$ e $x_{0}$. Dessa forma, temos
> $
> f(x)-f(x_0)=m(x-x_0)
> $
> Perceba que aqui, diferente da primeira abordagem, estamos partindo do fato de que a **reta tangente passa pelo ponto $(x_0,f(x_0))$**. Resta só a inclinação em relação a esse $x_0$ fixo e um ponto $(x,f(x))$ variável para determinar a reta tangente.
> 
> É por isso que aparece, sem mistério, o fator $(x−x_0)$ que precisa ser "cortado": ele é a marca algébrica de que $x_0$​ já é solução obrigatória de $f(x)=l(x)$. Cortar esse fator é o mesmo que perguntar: "tirando a solução $x_0$ que já sabíamos existir, o que sobra?"
> 
> 
> **Momento chave:**
> Em outras palavras, nós podemos dividir ambos os lados por $x-x_0$ porque estamos tentando achar uma solução **diferente** de $x_0$. Daí, acharemos condições para que exista uma solução diferente e, por fim, nós vamos ligar essa condição para descobrir qual a reta tangente.
> 
> Por fim, a gente descobre que, nesse caso, $x=\frac{m-b}{a}-x_{0}$. Então, esse é o segundo ponto de intersecção. O ponto é: nós queremos que esse segundo ponto seja igual a $x_{0}$ também! Então, tomamos $x=x_{0}$ e achamos que $m=2ax_{0}+b$.

Essa abordagem é interessante porque ela já carrega a essência da derivada. O que nós vamos fazer logo logo é usá-la em conjunto com a noção de limite para extrapolar nossa definição de reta tangente a uma função genérica, sem precisar ficar definindo o número de intersecções da reta com a função.


Vejamos agora o que podemos dizer do gráfico de $f(x)=x^{3}-2$. Parece razoável dizer que $l(x)=ax+b$ é tangente ao gráfico de $f$ se a equação $f(x)=l(x)$ tem exatamente **duas** soluções. Vejamos o que acontece nesse caso.

> [!container] 1ª abordagem.
> Na 1ª abordagem aqui, o Milton teve que misturar um pouco as duas abordagens que vimos na parábola: para reduzirmos a eq. do terceiro grau para uma do segundo, foi necessário fixar a reta genérica $l(x)=ax+b$ no ponto $(x_{0},f(x_{0}))$ e um outro ponto $(x,f(x))$. De posso de uma eq. do segundo grau, podemos analisar o discriminante. Como já temos o ponto $x_0$ fixado, queremos igualá-lo a zero de novo para ter duas soluções no total. No caso, a segunda solução não vai ser $x=x_0$ de novo tal qual no caso da parábola.
> 
> Na verdade, temos que analisar dois casos: o caso em que o discriminante é zero e o caso em que a eq. tem duas soluções, mas uma delas é igual a $x_0$. Para esse último, nós igualamos $x_0$ à raiz positiva SPG e vemos as condições que $a$ deve satisfazer. 
> 
> Geometricamente, esse caso representa a reta tangente que passaria por "dentro" do gráfico. Pela nossa def., temos duas retas tangentes à curva, só que uma delas não é tangente àquele ponto, mas sim àquele ponto lá embaixo (ver figura da pág 10). Por isso, precisamos adicionar um argumento geométrico à nossa definição.
> 
> O problema de quando igualamos o discriminante à zero é que nós forçamos a reta tangente a ter duas soluções iguais, mas diferentes de $x_0$. Agora, com essa nova abordagem, nós temos a solução original $x_0$ e estamos adicionando uma nova $x_0$ sem nem usar o discriminante. Assim, temos geometricamente uma reta tangente a esse ponto.

> [!exemplo] Exercício (análogo ao Método de Newton).
> **Exercício 1:** Mostre que para o polinômio geral de terceiro grau, $f(x)=a x^3+b x^2+c x+d$,
> $
> m\left(x_0\right)=3 a x_0^2+2 b x_0+c .
> $
> Notemos que a fórmula para $l(x)$ é
> $
> l(x)=3 x_{0}^2 x-2 x_0^3-2,
> $
> e que este reta intersecta o eixo $x$ em
> $
> \phi\left(x_0\right):=\frac{2}{3}\left(x_0+\frac{1}{x_0^2}\right) .
> $
> 
> **Exercício 2:** Considere a sequência $\left(x_n ; n \in \mathbb{N}_0\right)$ definida como $x_0=2$ e $x_n=\phi\left(x_{n-1}\right)$ para todo $n \in \mathbb{N}$. Prove que
> $
> \lim _{m \rightarrow \infty} x_n=\sqrt[3]{2}
> $


Pode ser que tenha algum truque algébrico que permita resolver essas equações no caso de polinômios de grau maior, dadas as respectivas definições de retas tangentes. Mesmo assim, calcular retas tangentes não é eficiente. Isso serve para introduzir o assunto e para implementar o método de newton.

Tentemos por exemplo definir a reta tangente para $f(x)=\cos(x)$. É muito complicado. Então, precisamos de uma definição mais robusta.



# Definição de Derivada

Quando a gente fala sobre derivada, o que faz sentido é **intervalo aberto** (vamos ver daqui a pouco o porquê).

> [!container]- Construindo a intuição da derivada.
> 
> Vamos pensar num caso geométrico simples (ver nota do Milton). Aqui, vamos supor que a função é bem comportada, pelo que é diferenciável. Logo, podemos calcular o valor da derivada tomando uma sequência particular, como uma crescente ou decrescente (isso não é verdade no caso geral).
> 
> Seja $f:(0,1) \rightarrow \mathbb{R}$ e seja $x \in (0,1)$. Seja $(x_{n};n \in \mathbb{N})$ em $(0,1)$ **crescente** com
> $
> \lim_{ n \to \infty } x_{n}=x, \;\; \text{ e } \;\; x_n \neq x \;\; \text{ para todo $n \in \mathbb{N}$}
> $
> Seja $l_{i}$ a reta que passa pelos pontos $(x_{i},f(x_{i})), (x,f(x))$.
> 
> A inclinação da reta $l_{i}$ é igual a
> $
> \frac{f(x)-f(x_{i})}{x-x_{i}}
> $ad-ps
* Só estamos interessados na inclinação da reta. Até porque a fórmula é fácil de se obter pela fórmula do ponto-inclinação.
```

> [!definicao]
> Seja $f:(a,b) \rightarrow \mathbb{R}$. Dizemos que $f$ é **diferenciável** em $x \in (a,b)$ se para toda sequência $(x_{n};n \in \mathbb{N})$ tal que
> $
> \lim_{ n \to \infty } x_{n}=x, \;\; \text{ e } \;\; x_n \neq x \;\; \text{ para todo $n \in \mathbb{N}$}
> $
> o limite
> $
> \lim_{ n \to \infty } \frac{f(x)-f(x_{i})}{x-x_{i}} =: f'(x)
> $
> existe.

Conforme já discutimos na sessão discussão em [[Continuidade]], o limite de uma sequência pode ou não tocar o valor real do limite (uma sequência $x_{n}=x$ por ex.). Acontece que aqui nós estamos por definição eliminando qualquer uma desses sequências, de modo que elas apenas se aproximem, mas nunca toquem o $x$. Se isso acontecesse, não teríamos como falar de reta que passa por um único ponto.

> [!obs]
> Aqui, é muito importante que a sequência $x_n$ seja **arbitrária**. Ela pode ser crescente, decrescente, oscilante, não importa. Assim, podemos garantir que o limite existe, independente da aproximação que fazemos. Veja o exemplo mais abaixo da função $f(x)=|\sin(x)|$.
> 
> As únicas condições que ela deve satisfazer são: ser convergente a $x$ e ser diferente de $x$ para todo $n$.

Se esse número tiver um limite, nós o chamaremos de **inclinação da reta tangente no ponto $x$**. 

O problema maior é que isso não vale para qualquer função $f$. Devem haver condições. 

E as condições para que esse limite exista não são tão fáceis. Em continuidade, nós tínhamos condições, como ser de Lipschitz, que é fácil de verificar que é suficiente (não necessária) para continuidade. No caso aqui, não há uma condição fácil de verificar que seja suficiente para que o limite exista. Então  nós vamos ter que fazer caso a caso.

> [!obs]- Por que o intervalo escrevemos o intervalo $(0,1)$ aberto?
> Porque nós queremos que essa condição $x_n \neq x \;\; \forall x$ seja verificada. E, para isso, nós precisamos de espaço. Se $x=0$, nós não teremos espaço para fazer isso pelo lado esquerdo, apenas pelo lado direito.

> [!obs]
> A princípio, esse limite podia **depender da sequência que tomarmos**. Podia ser que, se aproximássemos de dois jeitos diferente, a derivada desse algo diferente.
> 
> Mas, nessa definição aqui, isso não acontece. Se esse limite existir para qualquer sequência, então **todas** têm que ter o mesmo limite.

> [!exemplo]- Não diferenciável
> Um exemplo de coisa que não é diferenciável seria $f(x)=|\sin(x)|$. O que acontece com essa função?
> 
> Se nos aproximarmos do ponto zero pela esquerda ou pela direita, teremos retas tangentes diferentes. Portanto, essa função não é diferenciável em $x=0$.
> 
> ![[Pasted image 20260524112813.jpg|center|400]]
> 
> No caso, a retas tangentes seriam cada uma com 45° para esquerda e para direita. Antes, eu achava que ambas formariam uma reta de 90°, mas isso nunca é possível, pois, segundo nossa definição, a reta tangente deve poder ser descrita por uma função da forma $ax+b$.

Ver problema 3 da lista 9. O problema é de continuidade, mas o raciocínio é parecido: se queremos mostrar que uma função é contínua ou diferenciável num dado ponto, não podemos tomar uma sequência crescente por exemplo. Devemos tomar uma sequência arbitrária pelo mesmo argumento acima.


# Diferenciabilidade

> [!definicao]
> Se $f:(a,b)\rightarrow \mathbb{R}$ for diferenciável em $x$ para todo $x \in (a,b)$ dizemos que $f$ é diferenciável em $(a,b)$.

Conforme dito, não há uma condição fácil de verificar que seja suficiente para que o limite exista. No final das contas, para saber se uma função é diferenciável num dado ponto, nós devemos calcular o limite. Como subproduto do cálculo do limite, nós também provamos a sua **existência**. 

Como a inexistência da derivada se manifesta no cálculo do limite?

> [!lema]
> Se $f$ é **diferenciável** em $x_0$, então $f$ é **contínua** em $x_0$.

Ver demonstração na nota de aula 15.


Há vários motivos pelos quais uma função $f$ pode não ser diferenciável num dado ponto, como
* Não é contínua nesse ponto (contrapositiva do lema).
*  ele forma pico abrupto


# Derivada dos polinômios

Ver nota de aula 14-15 do Milton para ver as contas.

> [!obs] Derivada dos monômios $f(x)=x^l$.
> Antes de tomar o limite da def. de derivada, o Milton escreve a razão e vê se pode manipulá-la para deixá-la duma forma que seja mais propícia para fazer conta.
> 
> Afortunadamente, nós chegamos num produto notável e conseguimos cortar o termo $x_n-x$, pois isso nunca é zero pela nossa def. Depois nós usamos as propriedades elementares de limites: limite da soma e limite do produto. 
> 
> Assim, teremos tudo em função apenas do ponto $x$, que é o limite da sequência e também o ponto que tínhamos fixado inicialmente para a reta tangente.
> 
> O que estamos fazendo aqui é muito parecido em essência com a nossa 2ª abordagem do caso da parábola.

Pela linearidade do limite, para
$$
f(x):=\sum_{i=0}^{l} a_{i}\,x^{i},
$$
vemos que
$$
f'(x)=\sum_{i=1}^{l} i\,a_{i}\,x^{i-1}.
$$
Perceba que o índice foi de $0$ a $1$, porque o termo constante se anula. A função constante tem derivada zero, porque ela é uma reta com inclinação zero. Note-se que aquelas nossa definições iniciais de reta tangente não se aplicam para funções lineares, mas a definição com limite resolve isso: a constante tem derivada zero em particular (o numerador sempre se anula).


# Propriedades da derivada

[[Propriedades da derivada]]

* [[Teorema do Valor Médio]]
* [[Pontos Críticos]]
* [[A fórmula de Taylor]]

Ver [[Notação de Leibniz]].
