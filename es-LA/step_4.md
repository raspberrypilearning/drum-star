## Primera actualización

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Agregarás tu primera actualización. El botón **Conseguir redoblante** aparecerá al principio, para que el jugador o la jugadora sepa qué tambor tiene en mira.
</div>
<div>
![](images/first-upgrade.png){:width="300px"}
</div>
</div>

--- task ---

Agrega la imagen del **Drum-snare** a tu proyecto, cámbiale el nombre a "redoblante" y colócalo en el Escenario:

![](images/snare-stage.png)

--- /task ---

--- task ---

Arrastra el script `al hacer clic en este objeto`{:class="block3events"} de la imagen del **Platillo** al del **Redoblante**.

[[[scratch3-copy-code]]]

--- /task ---

--- task ---

Cambia los disfraces y el sonido del tambor.

Cambia el número de ritmos ganados a `2`:

![](images/snare-icon.png)

```blocks3
when this sprite clicked
+change [beats v] by [2] //2 beats per click
+switch costume to [drum-snare-b v] //hit costume
+play drum [(1) Snare Drum v] for [0.25] beats //drum sound
+switch costume to [drum-snare-a v] //not hit costume
```

--- /task ---

--- task ---

**Prueba:** Pon tu proyecto a prueba. Asegúrate de ganar 2 ritmos cuando hagas clic en el redoblante.

--- /task ---

Las actualizaciones no están disponibles cuando inicias el proyecto. Hay que ganárselas con los ritmos.

--- task ---

Agrega un script para ocultar el objeto del **tambor** al inicio del proyecto:

![](images/snare-icon.png)

```blocks3
when flag clicked
hide
```

--- /task ---

Un botón mostrará qué tambor es el próximo para actualizar y cuántos ritmos costará.

--- task ---

**Duplicar** el objeto de **Conseguir**:

![](images/duplicate-get.png)

Cambia la visibilidad a **Mostrar** y cámbiale el nombre a `Conseguir redoblante`. Colócalo en la esquina inferior derecha del Escenario:

![](images/get-snare.png)

--- /task ---

--- task ---

Haz clic en la imagen **Redoblante** y ve a la pestaña **Estilos**. Usa la herramienta (flecha) **Seleccionar** para resaltar el disfraz de tu tambor que no fue tocado. Haz clic en el icono **Grupo** y luego en **Copiar**:

![](images/snare-icon.png)

![](images/copy-costume.png)

--- /task ---

--- task ---

Haz clic en tu objeto **Conseguir redoblante** y **Pega** el disfraz del redoblante. Es posible que debas ajustar el tamaño y reubicarlo para que quepa en tu botón:

![](images/get-snare-icon.png)

![](images/paste-costume.png)

--- /task ---

--- task ---

Haz clic en la pestaña **Código** y agrega un script para mostrar el objeto **Conseguir redoblante** al inicio del proyecto:

![](images/get-snare-icon.png)

```blocks3
when flag clicked
show
```

--- /task ---

Solo se puede comprar la actualización si se tienen `10` o más ritmos. En [Haz crecer una libélula](https://projects.raspberrypi.org/en/projects/grow-a-dragonfly){:target="_blank"}, aprendiste a tomar decisiones con bloques `si`{:class="block3control"}.

Un bloque `si … sino`{:class="block3control"} se usa para tomar una decisión y realizará diferentes acciones si una condición es `cierta` o `falsa`.

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
Usamos <span style="color: #0faeb0">**si … sino**</span> todo el tiempo para tomar decisiones. Cuando te despiertas, compruebas `si`{:class="block3control"} es de mañana. Te levantas, o `sino`{:class="block3control"} te vuelves a dormir. ¿Puedes pensar en alguna decisión `si ... sino`{:class="block3control"} que hayas tomado? 
</p>

--- task ---

Agrega este código para obtener la actualización `si`{:class="block3control"} hay suficientes ritmos, o para `decir`{:class="block3looks"} `¡No hay suficientes ritmos!` si no se pueden actualizar:

![](images/get-snare-icon.png)

```blocks3
when this sprite clicked
if <(beats)>  [9]> then //if 10 or more beats
hide
change [beats v] by [-10] //take away the cost of upgrade
else
say [Not enough beats!] for [2] seconds 
end
```

--- /task ---

Hazle saber a los otros objetos y al Escenario que se compró la actualización para el redoblante.

--- task ---

Agrega un bloque `transmitir`{:class="block3events"} para enviar un nuevo mensaje `redoblante`:

![](images/get-snare-icon.png)

```blocks3
when this sprite clicked
if <(beats)>  [9]> then // if 10 or more beats
hide
change [beats v] by [-10] // take away the cost of upgrade
+ broadcast [snare v] // your drum name
else
say [Not enough beats!] for [2] seconds 
end
```

--- /task ---

--- task ---

Haz clic en el objeto **Redoblante**. Agrega este script:

![](images/snare-icon.png)

```blocks3
when I receive [snare v]
show
```

--- /task ---

Cuando actualices tu equipo, podrás tocar en lugares más grandes.

--- task ---

Agrega otro fondo. Elegimos **Chalkboard** para tocar en nuestro segundo concierto en la escuela.

Agrega el código al Escenario para `cambiar fondo`{:class="block3looks"} cuando se reciba el mensaje de actualización:

![](images/stage-icon.png)

```blocks3
when I receive [snare v]
switch backdrop to [Chalkboard v]
```

**Consejo:** Elige un lugar que sea una pequeña mejora al dormitorio. Desearás guardar los lugares más grandes para más adelante.

--- /task ---

--- task ---

**Prueba:** Ejecuta tu proyecto. Prueba y compra la actualización del redoblante antes de que tengas suficientes ritmos.

Cuando compras la verificación de actualización: el redoblante aparece, el botón desaparece, el lugar cambia y los `ritmos`{:class="block3variables"} descienden a `10`.

--- /task ---

--- save ---
