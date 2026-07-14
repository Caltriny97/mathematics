Data Criada: 22/05/2026 às 22:43
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

Nas notas de aula 11, 12 e 13 de cálculo do Milton foi bem recorrente a técnica de reduzir o problema original a um mais fácil de visualizar. Aqui vão algumas impressões de como e quando interpretar um problema de modo a simplificá-lo.

Basicamente, algo é sem perda de generalidade quando a demonstração daquele caso é exatamente igual à nossa simplificação.


- **Como foi usado nas suas notas:** * Na linearidade do limite, em vez de carregar $x_n \rightarrow x$, define-se uma <mark class="hltr-pink">nova sequência</mark> subtraindo o limite: $(x_n - x) \rightarrow 0$. O comportamento do limite não muda ao deslocá-lo para o zero.
    - No TVI e TVE, em vez de trabalhar em um intervalo genérico $[a, b]$, faz-se uma translação para começar em $0$.

> [!obs]
> A mudança de variável é algo que não afeta em nada nossas demonstrações. Basta nós descrevermos exatamente esse processo de transição com uma equivalência entre elas e trabalhar em diante com a nova variável definida.


- **Como foi usado nas suas notas:**
    - No TVI e TVE, o intervalo $[a, b]$ virou $[0, 1]$. A função foi "encolhida" para caber ali através de uma mudança de variável do tipo $g(x) = f(a + (b-a)x)$.
    - Na linearidade, assumiu-se $a, b \ge 0$. Se fossem negativos, o módulo $|a|$ e $|b|$ resolveria o sinal, mantendo a estrutura idêntica.

> [!obs]
> O ponto aqui é que: tudo o que fazemos pode ser desfeito depois (por isso a importância de sempre definir a transformação feita). Então, não perdemos generalidade.


# Considerações

No teorema da função inversa na aula 16, o Milton fez o seguinte encadeamento.
1. **Defina a função auxiliar:**  
    Seja \(g(x) = -f(x)\).
2. **Calcule a derivada de \(g(x)\):**  
    Pela regra da linearidade, \(g'(x) = -f'(x)\).
3. **Aplique a hipótese:**  
    Se a hipótese diz que \(f'(x) < 0\), então multiplicando por \(-1\) temos que \(g'(x) > 0\).
4. **Aplique o teorema original:**  
    Como $(g'(x) > 0)$, o teorema se aplica perfeitamente a \(g(x)\), garantindo que \(g\) possui uma inversa local diferenciável $(g^{-1}(y))$.
5. **Relacione as inversas:**  
    Como $(g(x) = -f(x))$, a função inversa de \(g\) se relaciona com a de \(f\) por:  
    $(g^{-1}(y)=f^{-1}(-y))$

---


> [!obs]
> Acho que isso têm muita relação com o problema 10 da lista 10 de Álgebra Linear. Lá, nós temos uma solução válida pra uma equação. Essa equação implica (só ida) em outras, que mantém o mesmo conjunto solução.
> 
> Aqui, nós definimos inicialmente uma regra de transformação. Essa regra implica em outros resultados e em algum momento resultará no mesmo resultado da nossa hipótese (se for SPG). Daí, resta desfazer a transformação no final do teorema e ver como os resultados se relacionam.