Data Criada: 06/04/2026 às 20:25
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

**Area**
Diferença entre $S_{inf}, S_{sup}$ e o supremo e o ínfimo delas, respectivamente. 


Definição para integrais não negativas

$3$ modos de definir funções limitadas(???), mas que podem assumir valores negativos
* Parte positiva e negativa
* Limitação por baixo
* Aproximação com sinal

Definição de partição do Andres para fazer análise de integrabilidade de funções. Ela me ajudar a identificar integrabilidade, mas me ajuda a calcular quanto é a integral?

Toda função de Lipschitz em $[a,b]$ é integrável
* demonstração geométrica do Milton
* demonstração via partição do Andres
* prova de que polinômios são integráveis (prova da lista e prova do Milton)

[[Funções Trigonométricas]]
* problema na definição de comprimento do arco
* duas abordagens para a função da área sob a curva do círculo trigonométrico
	* aula 5: mapeia essa área por $f(z)$ e subtrai do triângulo, sobrando só a área do arco. Daí, definimos $\theta$ em função dessa área, que está em função de $z$, que seria o $\text{sen}(\theta)$ da trigonometria. Ou seja, temos uma função $g(z)=\theta$: é a função $\text{arcsen}$
	* aula 6: 





# Os axiomas de área

Pelo axioma $2$, a área de elementos da classe $\mathcal{A}$ está bem definida.
[[Área]]

Agora, definiremos o ente geométrico "conjunto de ordenadas" (área sob o gráfico), cuja área desejamos calcular.


# Partições e a integral de funções em escada

Definiremos agora integral para funções em escada para depois chegar nas  funções mais gerais. Para tanto, é necessário dar uma definição analítica de função em escada, o que se consegue em termos do conceito de partição.
* [[Partições e funções em escada]]
	* nota do Andres
	* soma e produto de funções escada
	* definição de integral para funções em escada
	* propriedades da integral duma função em escada


# A integral de funções mais gerais

Uma vez definida a integral de funções em escada, o faremos agora a funções mais gerais de tal modo que a integral delas resultante goze de todas as propriedades referidas (ver no Apostol). Mas temos um problema: nem todas as funções podem ser aproximadas por defeito ou por excesso. Por isso, vamos nos restringir às funções **limitadas**.
* [[Definição de integral duma função limitada]] (num intervalo $[a,b]$)
	* Definição de integral duma função limitada
	* Integrais superior e inferior (nota da aula prática)


Uma vez definida **o que á a integral** de uma função **limitada** qualquer, vamos nos concentrar em responder as seguintes perguntas:
* (i) Quais as funções limitadas que são **integráveis**, ou seja, cuja integral existe de fato? (vamos analisar funções monótonas, Lipschitz, polinomiais...)
* (ii) Sabido que uma função $f$ é integrável, como **calcular** o integral de $f$ ?

Em outras palavras, a partir de agora vamos usar nossa definição de integral de funções limitadas para analisar a integrabilidade de classes de funções limitadas: funções monótonas, de Lipschitz, polinomiais...

Lembremos que nem toda função limitada é integrável (ex.: $\frac{1}{x}$). Por isso, é importante separar quais são integráveis ou não dentro das funções limitadas.

* [[Integral de funções monótonas limitadas]]
	* funções monótonas, estritamente monótonas e monótona por partes
	* integrabilidade e cálculo de funções **monótonas limitadas** (o que nós vimos até então geometricamente nas aulas do Milton). Mostramos primeiro que $\int_a^b t_n-\int_a^b s_n=\frac{C}{n}$ e, depois usamos para o valor numérico da integral o resultado do P1 da lista 2. 
	* Obs: claro que existem funções monótonas não limitadas (ex.: $f(x):=\sqrt{ x }$)
* [[Funções de Lipschitz]]


Vejamos agora algumas propriedades fundamentais da integral. No livro, elas foram herdadas das propriedades da integral de funções em escada (ver demonstrações).
* [[Propriedades fundamentais da integral]]


# Funções Trigonométricas

Vamos agora utilizar as noções de área para definir o ângulo $\theta$ no círculo trigonométrico. Assim, saberemos a integral em função do ângulo e, usando noção de função inversa, vamos definir integral de função $\sin, \cos$ e $\tan$ .
 [[Funções Trigonométricas]]