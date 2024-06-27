## Segunda atualização

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Suas habilidades na bateria estão melhorando. É hora de uma segunda atualização! Nesta etapa você escolherá qual tambor adicionar.
</div>
<div>
! [O cenário Holofote com um inseto.] (images/second-upgrade.png) {:width="300px"}
</div>
</div>

--- task ---

Duplique a atriz **Fada**:

![](images/duplicate-snare-drum.png)

--- /task ---

O sprite **Drum Costumes** tem muitas fantasias de bateria para você escolher.

--- task ---

Clique no ator **Varinha** e depois na aba **Sons**.

**Escolha:** um tambor para a próxima atualização. Escolhemos o **Batter**.

Arraste as fantasias 'hit' e 'not hit' da bateria escolhida para o seu novo sprite **Drum-snare2**:

![Imagem animada mostrando como arrastar fantasias de um sprite para outro.](images/drag-costumes.gif)

![O editor de pintura do novo sprite com duas fantasias adicionais na lista de fantasias.](images/drum-3-costumes.png)

--- /task ---

--- task ---

Dê um nome ao seu tambor de acordo com as fantasias que você escolheu.

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

Em seguida, você precisa de um botão para que os jogadores possam atualizar para esta nova bateria.

--- task ---

Duplique a atriz **Fada**.

Posicione-o no canto inferior direito do Palco. Mude seu nome para `Get` e depois o nome da sua nova bateria:

![A lista de Sprites com sprites 'Get snare' duplicados. O nome do sprite foi alterado para corresponder à nova bateria e posicionado no canto inferior direito do palco.](images/get-drum-3.png)

--- /task ---

--- task ---

Exclua a caixa **** da fantasia do botão. Copie e cole a fantasia 'not hit' da sua nova bateria na fantasia do botão.

Clique na ferramenta **Text** e altere o número para `30` para mostrar o custo do novo tambor.

Seu código deve ficar assim:

![O editor de pintura mostrando o novo traje do botão com a imagem e o texto do tambor escolhido foi atualizado para 30.](images/get-drum-copy.png)

--- /task ---


Este botão deve `ocultar`{:class="block3looks"} no início, depois `mostrar`{:class="block3looks"} quando o jogador atualizar para a caixa, para que ele saiba em qual bateria está trabalhando.

--- task ---

![](images/get-drum-3-icon.png)

```blocks3
when flag clicked
- show
+ hide
```

**Dica:** Para excluir um bloco, arraste-o para o menu Blocos ou clique com o botão direito e escolha **Excluir Bloco**. Em um computador, você também pode clicar em um bloco e tocar em <kbd>Excluir</kbd> para remover um bloco.

--- /task ---

--- task ---

Adicione um `quando eu receber`script {:class="block3events"} que seu novo botão de bateria mostrará como a próxima atualização quando o jogador obtiver o **Drum-snare** drum:

![](images/get-drum-3-icon.png)

```blocks3
when I receive [snare v] // appear when previous drum is bought
show // show button for next available drum
```

--- /task ---

--- task ---

Altere o número de batidas necessárias para comprar este tambor, e o número de batidas que são removidas, quando o jogador recebe este tambor.

Mude a mensagem que recebe `broadcast`{:class="block3events"} para o nome dos novos tambores. Crie uma nova mensagem com o nome da sua nova bateria:

![](images/get-drum-3-icon.png)

```blocks3
when this sprite clicked
if <(beats)>  [29]> then // change to 29
hide
change [beats v] by [-30] // change to 30
broadcast [conga v] // change to your drum name
else
say (join ((30) - (beats)) [beats needed!]) for [2] seconds
end
```

--- /task ---

--- task ---

Mude o `quando eu receber o script snare`{:class="block3events"} para `broadcast`{:class="block3events"} o nome da sua nova bateria. A bateria irá `mostrar`{:class="block3looks"} quando o jogador atualizar para a nova bateria:

![](images/drum-3-icon.png)

```blocks3
when I receive [conga v] // change to your drum name
show
```

--- /task ---

--- task ---

Adicione o ator **Giga**.

Adicione um script ao Palco para mudar o cenário quando o jogador atualizar para a nova bateria:

![](images/stage-icon.png)

```blocks3
when I receive [conga v] // change to your drum name
switch backdrop to (Party v)
```

--- /task ---

--- task ---

**Teste:** Clique na bandeira verde para iniciar o jogo e testar se você consegue ganhar batidas suficientes para conseguir sua nova bateria.

O que acontece se você clicar no botão antes de ganhar batidas suficientes?

--- /task ---

--- save ---
