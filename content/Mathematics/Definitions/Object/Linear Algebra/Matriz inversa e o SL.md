Data Criada: 10/04/2026 às 16:05
Tags:

Provado por:
Referências: [[Matriz Inversa]], [[Sistemas Lineares]]
Justificativas:

Especializações:
Generalizações:

> [!teorema] [[Matriz Inversa|Teorema.]]
> Seja $A_{n \times n}$ uma matriz quadrada. $A X=B$ possui uma única solução se, e somente se, $A$ é invertível.
> 
> **Prova.**
> Isso segue da unicidade da inversa. Caso a solução do sistema não fosse única e $A$ fosse invertível, haveria mais de uma matriz inversa, absurdo.

> [!obs]
> Para achar a solução única de um sistema $AX=B$, supondo $A$ invertível, temos dois dispositivos práticos:
> * $X=A^{-1}B$
> * escalonar a matriz aumentada $[A|B]$ até a FER, ou seja, ela estiver na forma $[I|S]$, onde $S$ é a solução.

