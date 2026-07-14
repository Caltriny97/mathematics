Data Criada: 28/03/2026 às 23:52
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

Tomemos, para um espaço bidimensional, $r = \{(x,y) \in R^{2};y=ax+b\}$ com $a,b \in \mathbb{R}$ fixos. Não é difícil ver que se trata da equação de uma reta. 

![[Pasted image 20260329004639.jpg|center|300]]

Perceba que, ao falarmos de equação de reta, estamos fazendo algo parecido com o que viemos feito em GA: temos uma coisa geométrica, a reta, e temos uma expressão algébrica que descreve as suas coordenadas através de uma equação.

Todas as retas podem ser descritas dessa forma acima? Não, a reta abaixo, por exemplo, não pode ser escrita dessa forma, porque não se trata de uma função. Quando escrevemos a equação da reta como $y = ax+b$, estamos assumindo que a reta pode representar o gráfico de uma função.

![[Pasted image 20260329004647.jpg|center|300]]


> [!discussao]- Funções e as retas.
> **O que é uma função?** Primeiro, precisamos definir o domínio e contradomínio e, depois, definir a regra da função. Por exemplo,
> $
> \begin{aligned}
> & f: \mathbb{R} \rightarrow \mathbb{R} \\
> & x \mapsto f(x) = y = ax+b
> \end{aligned}
> $
> A questão é que para ser uma função, para cada elemento do domínio, devemos associar um do contradomínio.
> 
> **E agora, o que é o gráfico de uma função?** 
> 
> **Mas antes, toda função tem gráfico?** Não, se fizermos o gráfico de $\mathbb{R}^{7} \times \mathbb{R}^{2022}$, não temos ideia de como desenhar isso num gráfico. Então são apenas alguns casos de funções bem particulares que vão ter gráfico. Podemos até fazer uma função cujo domínio não possa ser representada por um eixo, então perdemos essa ideia também. Mas, funções de $\mathbb{R} \mapsto \mathbb{R}$ ou de $\mathbb{R} \mapsto \mathbb{R}^{2}$ (curvas parametrizadas por exemplo) a gente consegue expressar o gráfico de alguma forma.
> 
> 
> Nós obviamente não poderíamos ter uma função cujo gráfico seja o abaixo, pois estaremos associando para $01$ valor de $x$ $03$ valores de $y$. Em outras palavras, para um curva ser o gráfico de uma função, nós nunca podemos ter em uma reta paralela ao eixo da imagem, mais de um ponto desse conjunto.
> 
> ![[Pasted image 20260331170255.jpg|center|500]]
> 
> Isso é o que acontece exatamente na figura abaixo (que mostramos anteriormente). Temos nela infinitos pontos associados um único $x$. Por isso, isso não é o gráfico de uma função de $x$ em relação a $y$... mas poderia ser de $y$ em relação a $x$. A gente convenciona colocar o domínio no eixo horizontal e o contradomínio, no horizontal. Mas poderíamos fazer uma representação diferente e colocar a imagem (ou contradomínio) da $f(x)$ no eixo horizontal, conforme a segunda figura.
> 
> ![[Pasted image 20260329004647.jpg|center|300]]
> 
> No caso abaixo, não conseguimos uma expressão $y=ax+b$ para defini-la, mas conseguimos um $x=ay+b$.
> 
> ![[Pasted image 20260331171607.jpg|center|300]]
> 
> Isso tudo é para entendermos que mesmo esses conceitos de função e gráfico de função são um pouco relativos. Temos que tomar cuidado para não estar pensando só no caso que nós geralmente lidamos.
> 
> 
> Essa abordagem usando função e gráfico de função é um jeito de conseguir uma equação pra reta.
> Dados dois pontos disjuntos que pertençam a uma reta, conseguimos sempre definir uma única reta que passa por eles. Agora, sabendo que ela descreve uma função, um jeito de tentar descobrir qual a equação dessa reta é simplesmente substituir os pontos, Daí caímos num **sistema linear** que conseguimos resolver e achar a equação. Sistema linear, retas, planos e matrizes vão estar associados o tempo todo...
> 
> Agora, se pegarmos os pontos $P_{0} = (1,3)$ e $P_{1} = (1,2)$, vamos cair num sistema sem solução, porque justamente estamos no caso de uma reta vertical que não pode ser representada por algo da forma $ax+b$. Isso não quer dizer que a reta não exista, apenas que a nossa suposição de que a reta é representada por essa forma está errada.
> 
> Um detalhe importante é que: essa ideia de que $y = ax+b$ é um reta sempre não é bem verdade, porque depende de que espaço isso está morando. Se for no $\mathbb{R}^{2}$, de fato representa uma reta. Agora, se for no $\mathbb{R}^{3}$, isso vai descrever um plano.
> 
> 

O ponto aqui é: nem toda reta pode ser escrita da forma $y = ax+b$ e essa equação ainda pode descrever outras coisas se não estivermos exatamente no $\mathbb{R}^{2}$. Então, é interessante a gente conseguir descrever retas de outras formas, outras equações e não só através de uma função, porque elas vão me dar aspectos diferentes do nosso elemento e nós vamos conseguir estudar ele de formas diferentes.

Se temos dois pontos disjuntos que estão na reta, nós conhecemos a reta. Mas veja também que, se nós conhecemos só o ponto $P_{0}$ e sabemos a direção da reta, nós também vamos conhecer a reta. Esse elemento que representa a direção da reta é o **vetor diretor**. Não nos importamos nem um pouco com o seu tamanho, nem o seu sentido. A única coisa que importa dele, do ponto de vista geométrico, é a **direção**.

Se temos dois pontos, conseguimos facilmente um ponto e o vetor diretor que é representado pelo segmento de reta $\overline{P_{0}P_{1}}$. Ambos são equivalentes.

Agora, vamos descrever os pontos da nossa reta de maneira diferente (o caso de $R^{3}$ é análogo para $\mathbb{R}^{2}$). Considerando que conhecemos um ponto $P_{0} = (x_{0}, y_{0},z_{0}$) e um vetor diretor $v=(v_{1},v_{2},v_{3})$, como podemos caracterizar o ponto $P=(x,y,x) \in r$?

![[Pasted image 20260331182050.png|center|200]]

Para o ponto $P$ azul estar na reta e o ponto $P$ vermelho não estar, precisamos tomar $\overline{P_{0}P}$ de modo que seja paralelo ao vetor diretor $v$. Em outras palavras,
$$
\begin{aligned}
P \in r & \Leftrightarrow \overrightarrow{P_0 P} / / v \\
& \Leftrightarrow \overrightarrow{P_0 P}=t v \text { para algum } t \in \mathbb{R} \\
& \Leftrightarrow\left(x-x_0, y-y_0, z-z_0\right)=t\left(v_1, v_2, v_3\right) \\
& \Leftrightarrow \underbrace{(x, y, z)}_P=\underbrace{\left(x_0, y_0, z_0\right)}_{P_0}+\underbrace{t\left(v_1, v_2, v_3\right)}_{\text {vetor (// v)}} \text { para algum } t \in \mathbb{R}
\end{aligned}
$$

> [!definicao] Definição.
> A soma de um ponto $P_0$ com um vetor $u$ é o ponto $P$ tal que o segmento orientado $\overrightarrow{P_0 P}$ é um representante de $u$.

> [!comentario]- Comentário.
> Um ponto menos outro ponto não dá um vetor matematicamente de forma precisa. A gente faz a conta para conseguir obter as coordenadas. Mas, na verdade, obtemos um vetor, que é o vetor $\overrightarrow{P_0 P}$ cujas coordenadas coincidem com pegar as coordenadas de $P$ e subtrair as coordenadas de $P_{0}$.


Essa equação que estamos obtendo aqui é outra forma muito comum de escrevermos a reta, porque ela nos diz imediatamente um ponto que pertence a reta e o vetor diretor e, com base nisso, caracteriza todos os outros. Essa é a **equação vetorial da reta**, porque o vetor diretor está explícito. Temos também as **equações paramétricas da reta** (paramétricas porque estão estamos colocando os pontos de uma curva, uma reta no caso, em função de uma variável), que na verdade é equivalente a vetorial, com a diferença de que as coordenadas estão separadas.

$$
\textbf{Eq. Vetorial da reta:}\quad
P=P_0+t v, \quad t \in \mathbb{R}
$$
$$
\textbf{Eqs. Paramétricas da reta:}\quad
\left\{\begin{array}{ll}
x & =x_0+t v_1 \\
y & =y_0+t v_2 \\
z & =z_0+t v_3
\end{array} \quad t \in \mathbb{R}\right.
$$

> [!obs]- O que mudou?
> Um detalhe interessante é que, se estivermos em $\mathbb{R}^{2}$ e não em $\mathbb{R}^{3}$, essas equações vão ser a mesma coisa. A diferença é que vamos ter uma coordenada a menos nos elementos no caso da vetorial e, no caso das paramétricas, vamos ter uma eq. a menos.
> 
> Enfim, essas duas equações funcionam muito bem para qualquer reta. Diferente daquela eq. inicial $y = ax+b$, que (i) é só pra $\mathbb{R}^{2}$ e (ii) não funcionava para retas verticais, essas duas formas de escrever a reta funcionam em qualquer caso. Qual a melhor delas? Depende do que queremos fazer, afinal cada uma representa coisas diferentes.
> 
> Se nós tivéssemos no $\mathbb{R}^{4}$ com essas equações só com $3$ termos, estaríamos definindo um [[subespaço vetorial]] de $\mathbb{R}^{4}$, que iria ser um hiperplano (dimensão 2). Agora, se adicionássemos um termo, seria ainda sim uma reta (só que em $4$ dimensões).

> [!obs]- Obs (sistema linear).
> Aqui, estamos num sistema linear, dependendo do que consideramos como variável: se não conhecemos $v_{1}$, nem $t$, não é um sistema linear (pois estaríamos multiplicando incógnitas). Agora, se conhecemos um ponto ($x_{0},y_{0}$ e $z_{0}$) e um vetor diretor ($v_{1}, v_{2}$ e $v_{3}$), aí é um sistema linear onde as nossas incógnitas são $x, y, z$ e $t$. Para verificar se um certo ponto está nessa reta, vamos resolver esse sistema linear (a princípio). Esse sistema é **possível e indeterminado** (tem $04$ incógnitas e $03$ equações), afinal ele descreve infinitos pontos.

Existem ainda mais dois tipos de formas de escrever reta (na verdade existem infinitas, mas ok):

$$
\textbf{Eqs. Simétricas da reta:}\quad 
$$
$$
\left(v_1, v_2\right. \text{ e } \left.v_3 \neq 0\right): \frac{x-x_0}{v_1}=\frac{y-y_0}{v_2}=\frac{z-z_0}{v_3}
$$

$$
\textbf{Eqs. Reduzidas da reta:}
$$
$$
\text{}\quad \left(v_1 \neq 0\right): \begin{cases}y & =m x+n \\ z & =p x+q\end{cases} 
$$
$$
\text{tal que }\quad m=\frac{v_2}{v_1}, p=\frac{v_3}{v_1}, n=y_0-\frac{v_2}{v_1} x_0 \text{ e } q=z_0-\frac{v_3}{v_1} x_0
$$
> [!obs]- Obs (restrições).
> A ideia da equação simétrica é isolar o $t$ nas $03$ equações paramétricas e, por fim, nos livramos do parâmetro. Por outro lado, a eq. simétrica nem sempre é possível, porque precisamos que o vetor diretor não tenha entradas nulas (ex.: $(1,0,1)$ não serviria).
> 
> Outra forma de escrever são as **eqs. reduzidas da reta**, que é parecida com o $y=ax+b$, só que pro caso de $03$ dimensões. Se for pra $02$ dimensões, teremos $y=mx+n$. Só que, pra isolar o $t$, precisamos $v_{1} \neq 0$, que é justamente o caso da reta vertical que falamos no início dessa nota (não descreve uma função).

> [!obs]- Sistema Linear e funções
> Na eq. vetorial e paramétrica, nós estamos lidando com um sistema linear (a princípio) em função do parâmetro $t$, que nada tem a ver com eixos do plano cartesiano. Por isso, conseguimos abstrair as retas para além do mundo dos gráficos de funções. A eq. simétrica é só uma simplificação disso (que acaba restringindo o nosso vetor direto). As eqs reduzidas por outro lado, tiram o parâmetro $t$ da jogada e voltam com a relação (função em outras palavras) entre eixos do plano cartesiano: $y$ e $z$ em função de $x$. Por isso, elas voltam a depender de que a nossa reta descreve uma função para representá-las.

> [!problema]- Problema.
> Verifique se $r=s$, onde $r: X = (t,2t,3t)$ e $s: X = (1-2t,2-4t,3-6t)$. Primeiro, vamos separar os termos que dependem de $t$ (o vetor diretor) e os que não dependem de $t$ (um ponto da reta). Fazemos isso baseado na nossa definição de operação de adição entre ponto e vetor. Depois, verificamos se as retas são paralelas, analisando os vetores diretores e, por fim, basta verificar que elas têm um ponto em comum.


# Subespaço Vetorial

> [!proposicao] Proposição.
> Considere as operações usuais de $\mathbb{R}^3$.
> * (i) Uma reta que passa pela origem determina um espaço vetorial.
> * (ii) Um plano que passa pela origem determina um espaço vetorial.

* [[Subespaços Vetoriais em GA]]


# Ângulo entre retas e planos

* [[Ângulo entre retas e planos]]