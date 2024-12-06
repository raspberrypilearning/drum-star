## Segunda actualización

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Tus habilidades con los tambores están mejorando. ¡Es hora de una segunda actualización! En este paso, elegirás qué tambor agregar.
</div>
<div>
![El Escenario muestra un fondo de la fiesta con 3 tambores.](images/second-upgrade.png){:width="300px"}
</div>
</div>

--- task ---

Duplica la imagen del **Redoblante**:

![](images/duplicate-snare-drum.png)

--- /task ---

El objeto **Drum Costumes** tiene muchos disfraces de tambores para elegir.

--- task ---

Haz clic en el objeto **Drum Costumes** y selecciona la pestaña **Disfraces**.

**Elige:** un tambor para la próxima actualización. Elegimos **Conga**.

Arrastra los disfraces 'hit' y 'not hit' del tambor elegido a tu nuevo objeto **Redoblante2**:

![Imagen animada que muestra cómo arrastrar disfraces de una imagen a otra.](images/drag-costumes.gif)

![El editor de pintura del nuevo objeto con dos disfraces adicionales en la lista de disfraces.](images/drum-3-costumes.png)

--- /task ---

--- task ---

Dale un nombre a tu tambor para que coincida con los disfraces que elegiste.

![](images/drum-3-named.png)

--- /task ---

--- task ---

Haz clic en la pestaña **Código**. Cambia el código para usar los disfraces correctos y elige un sonido para tu nuevo tambor.

Cambia el número de ritmos que ganas haciendo clic en el nuevo tambor a `5`:

![](images/drum-3-icon.png)

```blocks3
when this sprite clicked
+change [ritmos v] by [5] //5 ritmos por clic
+switch costume to [ v] //tu estilo tocado
+play drum [ v] for [0.25] beats //tu sonido de tambor
+switch costume to [ v] //tu estilo sin tocar
```

--- /task ---

--- task ---

Arrastra tu nuevo tambor a su posición en el Escenario:

![Tambor nuevo a la derecha de los demás tambores.](images/drum-3-positioned.png)

--- /task ---

A continuación, necesitas un botón para que los jugadores puedan actualizar a este nuevo tambor.

--- task ---

Duplica el objeto **Conseguir redoblante**.

Colócalo en la esquina inferior derecha del Escenario. Cambia su nombre a `Conseguir` seguido del nombre de tu nuevo tambor:

![La lista de objetos con el objeto 'Conseguir redoblante' duplicado. El nombre de la imagen cambió para coincidir con el nuevo tambor y se colocó en la parte inferior derecha del Escenario.](images/get-drum-3.png)

--- /task ---

--- task ---

Elimina el **redoblante** del disfraz del botón. Copia y pega el disfraz 'sin tocar' para tu nuevo tambor en el disfraz del botón.

Haz clic en la herramienta **Texto** y cambia el número a `30` para mostrar el precio del nuevo tambor.

Tu botón debería verse así:

![El editor de pintura que muestra el nuevo disfraz del botón con la imagen del tambor elegido y el texto actualizado a 30.](images/get-drum-copy.png)

--- /task ---


Este botón se debe `ocultar`{:class="block3looks"} al principio, luego `aparecer`{:class="block3looks"} cuando se actualice al redoblante, para que se sepa qué tambor está en la mira.

--- task ---

![](images/get-drum-3-icon.png)

```blocks3
when flag clicked
- show
+ hide
```

**Sugerencia:** Para eliminar un bloque, arrástralo al menú Bloques o haz clic con el botón derecho y elije **Eliminar bloque**. En una computadora, también puedes hacer clic en un bloque y luego presionar el botón <kbd>Eliminar bloque</kbd> para eliminar un bloque.

--- /task ---

--- task ---

Agrega una secuencia de comandos `al recibir`{:class="block3events"} que el nuevo botón de tambor mostrará como la próxima actualización cuando se obtenga el tambor **Redoblante**:

![](images/get-drum-3-icon.png)

```blocks3
when I receive [redoblante v] // aparecer cuando se compra el tambor anterior
show // mostrar el botón para el siguiente tambor disponible
```

--- /task ---

--- task ---

Cambia la cantidad de ritmos necesarios para comprar este tambor y la cantidad de ritmos que se eliminan cuando se obtiene este tambor.

Also change the message that se `envía`{:class="block3events"} cuando el jugador obtiene un unuevo tambor. Crea un nuevo mensaje con el nombre de tu nuevo tambor:

![](images/get-drum-3-icon.png)

```blocks3
when this sprite clicked
if <(ritmos)>  [29]> then // cambiar a 29
hide
change [ritmos v] by [-30] // cambiar a 30
broadcast (conga v) // cambiar a tu nombre de tambor
else
say [¡No hay suficientes ritmos!] for [2] seconds 
end
```

--- /task ---

--- task ---

También cambia `al recibir redoblante`{:class="block3events"} por `transmitir`{:class="block3events"} el nombre de tu nuevo tambor. El tambor va a`aparecer`{:class="block3looks"} cuando se actualice al nuevo tambor:

![](images/drum-3-icon.png)

```blocks3
when I receive [conga v] // cambiar a tu nombre de tambor
show
```

--- /task ---

--- task ---

Agrega el fondo **Party**.

Agrega una secuencia de comandos al Escenario para cambiar el fondo cuando se actualice al nuevo tambor:

![](images/stage-icon.png)

```blocks3
when I receive [conga v] // cambiar a tu nombre de tambor
switch backdrop to (Party v)
```

--- /task ---

--- task ---

**Prueba:** Haz clic en la bandera verde para iniciar el juego y prueba que puedas ganar suficientes ritmos para así conseguir tu nuevo tambor.

¿Qué sucede si haces clic en el botón antes de haber ganado suficientes ritmos?

--- /task ---

--- save ---
