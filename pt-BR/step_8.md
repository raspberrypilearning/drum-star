## Challenge

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Atualize seu projeto com mais bateria e mais cenários enquanto toca em locais mais incríveis. 
</div>
<div>
![](images/upgrade-project.png){:width="300px"}
</div>
</div>

### Add more drums

To add another drum to unlock, look back at the earlier steps of the project.

Here are some reminders if you need them.

--- collapse ---

---
title: For the drum
---

--- task ---

Duplique o sprite **drum** anterior e adicione duas fantasias.

--- /task ---

--- task ---

Altere o traje ``{:class="block3looks"} e `som`{:class="block3sound"} usado no script `quando este sprite clicou em`{:class="block3events"} script.

--- /task ---

--- task ---

Altere o número de `batidas`{:class="block3variables"} obtidas no script `quando este sprite clicou em`{:class="block3events"}.

--- /task ---

--- task ---

Mude a mensagem ``{:class="block3events"} que faz o tambor `mostrar`{:class="block3looks"} para uma mensagem para o **novo tambor**.

--- /task ---

--- /collapse ---

--- collapse ---

---
title: For the 'Get' button
---

--- task ---

Duplicar o **Obtenha** sprite.

--- /task ---

--- task ---

Altere a mensagem ``{:class="block3events"} que faz o botão aparecer para a `mensagem`{:class="block3events"} `transmissão`{:class="block3events"} pelo **tambor anterior**.

--- /task ---

--- task ---

Troque a fantasia `por`{:class="block3looks"} incluindo o custo do novo tambor.

--- /task ---

--- task ---

Change the number of `beats`{:class="block3variables"} you must have to unlock this drum in the `if`{:class="block3events"} condition. Change the negative number of `beats`{:class="block3variables"} you `change by`{:class="block3variables"} when you unlock this drum. Altere o número de `batidas`{:class="block3variables"} obtidas no script `quando este sprite clicou em`{:class="block3events"}. Change the message that is `broadcast`{:class="block3events"} to the name of the **new drum**.

--- /task ---

--- /collapse ---

--- collapse ---

---
title: For the venue
---

--- task ---

Adicionar um plano de fundo.

--- /task ---

--- task ---

Add a script to the Stage to `switch backdrop to`{:class="block3looks"} the new backdrop when the `message`{:class="block3events"} for this drum is received.

--- /task ---

Você pode descobrir que sua bateria precisa estar em uma nova posição em um cenário diferente.

--- task ---

Adicione um script começando com `quando o cenário mudar para`{:class="block3events"} para cada sprite **tambores** com um bloco `vá para`{:class="block3motion"} para fazê-los mudar de posição.

O ônibus precisa estar na sua posição inicial `quando bandeira verde for clicada em`{: class = "block3events"}.

--- /task ---

--- /collapse ---

### Improve feedback to the player

Tell the player exactly **how many more** beats are needed to unlock the next drum.

--- task ---

Add this code to `join`{:class="block3operators"} the number of beats needed with the text you have used to tell the player they need more beats if they do not have enough to unlock the next drum:

```blocks3
when this sprite clicked
if <(beats)>  [9]> then //if 10 or more beats
hide
change [beats v] by [-10] //take away the cost of upgrade
else
+ say (join ((10) - (beats)) [beats needed!]) for [2] seconds
end
```

**Note**: Update the numbers to match those needed to unlock each drum.

--- /task ---

### Tidy your code

--- task ---

**Tidy:** If you have time, then it's a good idea to make sure the sprites in the sprite list are in a sensible order, starting with the drums in their locked order and then the buttons in order.

--- /task ---

--- task ---

### Stuck?

**Debug:** Primeiro certifique-se de realmente entender quando a bateria e os botões devem aparecer e como a variável `beats`{:class="block3variables"} deve mudar. É muito mais fácil depurar um projeto se você tiver certeza do que ele deve fazer.

--- collapse ---
---
title: My drum doesn't show/hide correctly
---

A menos que seja o primeiro tambor, seu tambor deve ter um script `quando flag clicado`{:class="block3events"} para `ocultar`{:class="block3looks"}.

It should have a `when I receive`{:class="block3events"} `this drum` script to `show`{:class="block3looks"}.

Verifique se o botão **Get** para este tambor `transmite`{:class="block3events"} a mesma mensagem.

--- /collapse ---

--- collapse ---
---
title: My Get button doesn't show/hide correctly
---

A menos que o botão seja para o primeiro tambor, ele deve `ocultar`{:class="block3looks"} `quando o sinalizador for clicado`{:class="block3events"}.

It should `show`{:class="block3looks"} `when I receive`{:class="block3events"} the message for the **previous drum**.

The **Get** button should `show`{:class="block3looks"} to let the player know about the next drum they can unlock.

--- /collapse ---

--- collapse ---
---
title: I can unlock a drum when I don't have enough beats
---

Verifique se você alterou o número de `batidas`{:class="block3variables"} necessárias `quando este sprite clicou em`{:class="block3events"} no script para o botão **Get** da bateria.

--- /collapse ---

--- collapse ---
---
title: The number of beats doesn't change correctly when I unlock a new drum
---

Verifique se você alterou o número de `batidas`{:class="block3variables"} necessárias `quando este sprite clicou em`{:class="block3events"} no script para o botão **Get** da bateria.

Certifique-se de que corresponda ao número na fantasia do botão da bateria.

--- /collapse ---

--- /task ---

**Dica:** Se você ficar realmente confuso, não há problema em excluir o novo tambor e seu botão e começar de novo. Às vezes é difícil detectar um bug.

--- save ---
