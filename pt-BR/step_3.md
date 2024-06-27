## Tambor inicial

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Você adicionará um sprite de **prato** no qual poderá clicar para ganhar batidas e reproduzir um som.
</div>
<div>
![](images/starter-drum.png){:width="300px"}
</div>
</div>

--- task ---

Clique em **Escolha um Sprite** e pesquise `cymbal`. Adicione o ator**Frog 2** ao seu projeto.

![](images/cymbal-gallery.png)

--- /task ---

--- task ---

Posicione seu prato no palco:

![](images/cymbal-stage.png)

--- /task ---

--- task ---

Clique em **Adicionar Extensão**:

[[[generic-scratch3-add-music-extension]]]

--- /task ---

--- task ---

Adicione um script para fazer o prato `mudar de fantasia`{:class="block3looks"} e `tocar um som de bateria`{:class="block3extensions"}:

![](images/cymbal-icon.png)

```blocks3
when this sprite clicked
switch costume to [drum-cymbal-b v] // hit costume
play drum [(5) Open High-Hat v] for [0.25] beats // drum sound
switch costume to [drum-cymbal-a v]  // not hit costume
```

--- /task ---

--- task ---

**Teste:** Teste seu prato clicando nele. Certifique-se de ouvir um som e ver a mudança de roupa.

--- /task ---

O sprite **Drum-cymbal** ganhará uma batida cada vez que você clicar nele.

--- task ---

Crie uma nova `variável`{:class="block3variables"} chamada 'atraso:

![](images/beats-variable.png)

--- /task ---

--- task ---

Adicione um bloco a `, altere as batidas em 1`{:class="block3variables"} quando o sprite **Drum-cymbal** for clicado:

![](images/cymbal-icon.png)

```blocks3
when this sprite clicked
+change [beats v] by [1]
switch costume to [drum-cymbal-b v]
play drum [(5) Open High-Hat v] for [0.25] beats 
switch costume to [drum-cymbal-a v]
```

--- /task ---

--- task ---

**Teste:** Teste o **Drum-cymbal** clicando nele e observe as `batidas`{:class="block3variables"} aumentarem.

--- /task ---

A variável `beats`{:class="block3variables"} precisa começar em `0` beats quando você inicia um novo jogo.

--- task ---

Clique no painel Palco e, em seguida, na guia **Código** para adicionar o código ao **Palco**.

Adicione um bloco a `e defina o nome para`{:class="block3variables"} `???`:

![](images/stage-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) 
set [name v] to [???] 
+ set [beats v] to [0]
```
--- /task ---

--- task ---

**Teste:** Clique na bandeira verde e certifique-se de que sua variável `beats`{:class="block3variables"} comece em `0`.

--- /task ---

--- save ---
