## More drums!

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Nesta etapa você escolherá qual tambor adicionar.
</div>
<div>
! [O cenário Holofote com um inseto.] (images/second-upgrade.png) {:width="300px"}
</div>
</div>

--- task ---

Duplique a atriz **Fada**:

![](images/duplicate-snare-drum.png)

--- /task ---

--- task ---

Clique no ator **Varinha** e depois na aba **Sons**.

**Choose:** which drum to unlock next. Escolhemos o **Batter**.


--- /task ---

--- task ---

Arraste as fantasias 'hit' e 'not hit' da bateria escolhida para o seu novo sprite **Drum-snare2**:

![Imagem animada mostrando como arrastar fantasias de um sprite para outro.](images/drag-costumes.gif)

![O editor de pintura do novo sprite com duas fantasias adicionais na lista de fantasias.](images/drum-3-costumes.png)

--- /task ---

--- task ---

Name the new drum to match the costumes you chose.

![](images/drum-3-named.png)

--- /task ---

--- task ---

Clique na guia **Código'**. Altere o código para usar as fantasias corretas e escolha um som para sua nova bateria.

Altere o número de batidas que você ganha clicando no novo tambor para `5`:

![](images/drum-3-icon.png)

```blocks3
when this sprite clicked
+change [beats v] by [5] //5 beats per click
+switch costume to [ v] //your hit costume
+play drum [ v] for [0.25] beats //your drum sound
+switch costume to [ v] //your not hit costume
```

--- /task ---

--- task ---

Arraste sua nova bateria para a posição no Palco:

![Novo tambor à direita dos outros tambores.](images/drum-3-positioned.png)

--- /task ---

Add a button so that players can unlock the new drum.

--- task ---

Duplicate the **Get snare** sprite and position it in the bottom-right corner of the Stage.

--- /task ---

--- task ---

Change its name (for example `Get conga`):

![The Sprite list with duplicated 'Get snare' sprite. The sprite name has been changed to match the new drum type and positioned in the bottom-right of the Stage.](images/get-drum-3.png)

--- /task ---

--- task ---

Delete the **snare drum** from the new 'Get' button costume.

--- /task ---

--- task ---

Copy the 'not hit' costume for your new drum and paste it to the new 'Get' button costume.

--- /task ---

--- task ---

Clique na ferramenta **Text** e altere o número para `30` para mostrar o custo do novo tambor.

![O editor de pintura mostrando o novo traje do botão com a imagem e o texto do tambor escolhido foi atualizado para 30.](images/get-drum-copy.png)

--- /task ---

Your new 'Get' button should `hide`{:class="block3looks"} at the start.

--- task ---

![](images/get-drum-3-icon.png)

```blocks3
when flag clicked
+ hide
```

--- /task ---

--- task ---

Add a `when I receive`{:class="block3events"} script that your new 'Get' button will `show`{:class="block3looks"} when the player unlocks the snare drum.

```blocks3
when I receive [snare v] // appear when previous drum is unlocked
show // show button to get the new drum
```

--- /task ---

--- task ---

Change:
- The number of beats needed to unlock this drum
- The number of beats that are removed when the player unlocks this drum.
- The message that is `broadcast`{:class="block3events"} when the player gets the new drum.

```blocks3
when this sprite clicked
if <(beats)>  [29]> then // change to 29
hide
change [beats v] by [-30] // change to -30
broadcast (conga v) // change to your drum name
else
say [More beats needed!] for [2] seconds 
end
```

--- /task ---

--- task ---

Click your new drum sprite and change the `when I receive snare`{:class="block3events"} script to show it when your new drum is unlocked:

```blocks3
when I receive [conga v] // change to your drum name
show
```

--- /task ---

--- task ---

Adicione o ator **Giga**.

--- /task ---

--- task ---

Adicione um script ao Palco para mudar o cenário quando o jogador atualizar para a nova bateria:

![](images/stage-icon.png)

```blocks3
when I receive [conga v] // change to your drum name
switch backdrop to (Party v)
```

--- /task ---

--- task ---

**Test:** Click the green flag to start the game.

You should unlock your new drum if you earn enough beats.

What happens if you click the button before you have earned enough beats?

--- /task ---

--- save ---
