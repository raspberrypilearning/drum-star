## Challenge

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Mejora tu proyecto con más tambores y más fondos mientras tocas en lugares más increíbles. 
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

Duplica el objeto del **tambor** anterior y agregar dos disfraces.

--- /task ---

--- task ---

Cambiar el `disfraz`{:class="block3looks"} y el `sonido`{:class="block3sound"} que se usan en el script `al hacer clic en este objeto`{:class="block3events"}.

--- /task ---

--- task ---

Cambia el número de `ritmos`{:class="block3variables"} que se ganan en el script `al hacer clic en este objeto`{:class="block3events"}.

--- /task ---

--- task ---

Cambia el `mensaje`{:class="block3events"} que hace que el tambor se `muestre`{:class="block3looks"} a uno para el **nuevo tambor**.

--- /task ---

--- /collapse ---

--- collapse ---

---
title: For the 'Get' button
---

--- task ---

Duplica el objeto **Conseguir** anterior.

--- /task ---

--- task ---

Cambiar el `mensaje`{:class="block3events"} que hace aparecer al botón en el`mensaje`{:class="block3events"} `transmitir`{:class="block3events"} por el **tambor anterior**.

--- /task ---

--- task ---

Cambiar el `disfraz`{:class="block3looks"} incluyendo el precio del nuevo tambor.

--- /task ---

--- task ---

Change the number of `beats`{:class="block3variables"} you must have to unlock this drum in the `if`{:class="block3events"} condition. Change the negative number of `beats`{:class="block3variables"} you `change by`{:class="block3variables"} when you unlock this drum. Change the number that `beats`{:class="block3variables"} needs to be subtracted from in the `join`{:class="block3operators"} block. Change the message that is `broadcast`{:class="block3events"} to the name of the **new drum**.

--- /task ---

--- /collapse ---

--- collapse ---

---
title: For the venue
---

--- task ---

Agrega un nuevo fondo.

--- /task ---

--- task ---

Add a script to the Stage to `switch backdrop to`{:class="block3looks"} the new backdrop when the `message`{:class="block3events"} for this drum is received.

--- /task ---

Es posible que descubras que tus tambores deben estar en una nueva posición sobre un fondo diferente.

--- task ---

Add a script starting with `when backdrop changes to`{:class="block3events"} to each **drum** sprite with a `go to`{:class="block3motion"} block to make them change position.

También deberás fijar tu posición inicial en `al hacer clic en la bandera`{:class="block3events"}.

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

**Debug:** Primero, asegúrate de comprender realmente cuándo deberían los tambores y los botones aparecer y cómo debe cambiar la variable `ritmos`{:class="block3variables"}. Es mucho más fácil depurar un proyecto si tienes claro lo que se supone que debes hacer.

--- collapse ---
---
title: My drum doesn't show/hide correctly
---

A menos que sea el primer tambor, debería tener un script `cuando se hace clic en la bandera`{:class="block3events"} para poderse `ocultar`{:class="block3looks"}.

It should have a `when I receive`{:class="block3events"} `this drum` script to `show`{:class="block3looks"}.

Comprueba que el botón **Conseguir** para este tambor `envía`{:class="block3events"} el mismo mensaje.

--- /collapse ---

--- collapse ---
---
title: My Get button doesn't show/hide correctly
---

A menos que el botón sea para el primer tambor, se debería `ocultar`{:class="block3looks"} `cuando se hace clic en la bandera`{:class="block3events"}.

It should `show`{:class="block3looks"} `when I receive`{:class="block3events"} the message for the **previous drum**.

The **Get** button should `show`{:class="block3looks"} to let the player know about the next drum they can unlock.

--- /collapse ---

--- collapse ---
---
title: I can unlock a drum when I don't have enough beats
---

Comprueba que hayas cambiado el número de `ritmos`{:class="block3variables"} necesarios `al hacer clic en este objeto`{:class="block3events"} en el del botón **Conseguir** para el tambor.

--- /collapse ---

--- collapse ---
---
title: The number of beats doesn't change correctly when I unlock a new drum
---

Comprueba que hayas`cambiado ritmos en`{:class="block3variables"} un número negativo `al hacer clic en este objeto`{:class="block3events"} en el script del botón **Conseguir** para el tambor.

Asegúrate de que coincida con el número del disfraz del botón.

--- /collapse ---

--- /task ---

**Consejo:** Si te confundes, no hay problema si eliminas el nuevo tambor y su botón y comienzas de nuevo. A veces es difícil detectar un error.

--- save ---
