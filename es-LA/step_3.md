## Tambor de principiante

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Agregarás una imagen de un **platillo** en el que puedes hacer clics para ganar ritmos y reproducir un sonido.
</div>
<div>
![](images/starter-drum.png){:width="300px"}
</div>
</div>

--- task ---

Haz clic en **Elegir un objeto** y busca `cymbal`. Agrega la imagen del **Drum-cymbal** a tu proyecto y cambia el nombre a "platillo".

![](images/cymbal-gallery.png)

--- /task ---

--- task ---

Coloca tu platillo en el Escenario:

![](images/cymbal-stage.png)

--- /task ---

--- task ---

Agrega la **Extensión musical**:

[[[generic-scratch3-add-music-extension]]]

--- /task ---

--- task ---

Agrega una secuencia de comandos para hacer `cambiar disfraz a`{:class="block3looks"} y `reproducir un sonido de bateria`{:class="block3extensions"} al platillo:

![](images/cymbal-icon.png)

```blocks3
when this sprite clicked
switch costume to [drum-cymbal-b v] // estilo tocado
play drum [(5) Open High-Hat v] for [0.25] beats // sonido de tambor
switch costume to [drum-cymbal-a v]  // estilo sin tocar
```

--- /task ---

--- task ---

**Prueba:** Prueba tu platillo haciendo clic en él. Asegúrate de escuchar un sonido y que cambie el disfraz.

--- /task ---

La imágen del **Platillo** te otorgará un ritmo cada vez que hagas clic en él.

--- task ---

Crea una `variable`{:class="block3variables"} llamada `ritmos`:

![](images/beats-variable.png)

--- /task ---

--- task ---

Agrega un bloque para `cambiar ritmos en 1`{:class="block3variables"} cuando hagas clic en la imagen del **Platillo**:

![](images/cymbal-icon.png)

```blocks3
when this sprite clicked
+change [ritmos v] by [1]
switch costume to [drum-cymbal-b v]
play drum [(5) Open High-Hat v] for [0.25] beats 
switch costume to [drum-cymbal-a v]
```

--- /task ---

--- task ---

**Prueba:** Haz clic en el **Platillo** para probar y observa cómo aumentan los `ritmos`{:class="block3variables"}.

--- /task ---

La variable `ritmos`{:class="block3variables"} debe comenzar en `0`cuando comienzas un nuevo juego.

--- task ---

Haz clic en el panel Escenario y luego en la pestaña **Código** para añadirle el código al escenario.

Agrega un bloque `fijar ritmos a`{:class="block3variables"} `0`:

![](images/stage-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) 
set [nombre v] to [???] 
+ set [ritmos v] to [0]
```
--- /task ---

--- task ---

**Prueba:** Haz clic en la bandera verde y asegúrate de que tu variable `ritmos`{:class="block3variables"} comienza en `0`.

--- /task ---

--- save ---
