
--- question ---

---
legenda: Pergunta 3 de 3
---

Você usou este script para controlar o que acontece quando o jogador clica no botão para atualizar sua bateria:

```blocks3
when this sprite clicked
if <(beats)>  [29]> then 
hide
change [beats v] by [-30] 
broadcast (conga v) 
else
say [Not enough beats!] for [2] seconds 
end
```

Se o valor da variável `batidas`{:class="block3variables"} for `29`, o que acontecerá quando o jogador clicar no botão?

--- choices ---

- ( ) O sprite irá `ocultar`{:class="block3looks"}

  --- feedback ---

  Não exatamente, há um bloco `hide`{:class="block3looks"} no script, mas ele não será executado com `29` `batidas`{:class="block3variables"}. Dê uma olhada no roteiro novamente.

  --- /feedback ---

- (x) O sprite do botão `dirá`{:class="block3looks"} `Batidas insuficientes!`

  --- feedback ---

Sim, a condição verifica se `batidas`{:class="block3variables"} é maior que `29`, mas `batidas`{:class="block3variables"} é igual a `29` então o jogador não tem o suficiente.

  --- /feedback ---

- ( ) 30 será subtraído do valor da variável `batidas`{:class="block3variables"}

  --- feedback ---

  Você usou a variável `batidas`{:class="block3variables"} para armazenar um número. `batidas`{:class="block3variables"} é `29` o que significa `batidas`{:class="block3variables"} `> 29` é falso, então os blocos na primeira parte de `if`{:class O bloco ="block3control"} não será executado.

  --- /feedback ---

- ( ) Nada

  --- feedback ---

  Não, o script sempre fará alguma coisa. Dê uma olhada mais de perto para ver qual parte do script será executada quando você tiver `29` `batidas`{:class="block3variables"}.

  --- /feedback ---

--- /choices ---

--- /question ---
