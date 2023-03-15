## Mejora tu proyecto

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Mejora tu proyecto con más tambores y más fondos mientras tocas en lugares más increíbles. 
</div>
<div>
![](images/upgrade-project.png){:width="300px"}
</div>
</div>

Hay muchos más estilos de tambores por elegir para agregar más actualizaciones a tu proyecto.

Para agregar otra mejora de tambor, revisa los pasos anteriores del proyecto.

Para el **tambor**, deberás:

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

Para el **botón**, deberás:

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

Cambia el número de `ritmos`{:class="block3variables"} que debes poseer para conseguir este tambor en la condición `si`{:class="block3events"}. Cambia el número negativo de `ritmos`{:class="block3variables"} al `cambiar por`{:class="block3variables"} cuando consigas este tambor. Cambia el mensaje que recibe `transmitir`{:class="block3events"} por el nombre de los **nuevos tambores**.

--- /task ---

Para el **lugar**, deberás:

--- task ---

Agrega un nuevo fondo.

--- /task ---

--- task ---

Agrega un script al Escenario para `cambiar fondo a`:class="block3looks"} el nuevo fondo cuando se reciba el `mensaje`{:class="block3events"} para este tambor.

--- /task ---

Es posible que descubras que tus tambores deben estar en una nueva posición sobre un fondo diferente.

--- task ---

Agrega un script que comience con `cuando el fondo cambia a`{:class="block3events"} para cada objeto de **tambor** con un bloque `ir a`{:class="block3motion"} para que cambie de posición.

También deberás fijar tu posición inicial en `al hacer clic en la bandera`{:class="block3events"}.

--- /task ---

--- task ---

**Ordernar:** Si tienes tiempo, es una buena idea asegurarte de que los objetos en la lista sigan un orden sensato, comenzando por los tambores con su orden de actualización y siguiendo con los botones en orden.

--- /task ---

--- task ---

**Debug:** Primero, asegúrate de comprender realmente cuándo deberían los tambores y los botones aparecer y cómo debe cambiar la variable `ritmos`{:class="block3variables"}. Es mucho más fácil depurar un proyecto si tienes claro lo que se supone que debes hacer.

--- collapse ---
---
title: Mi tambor no aparece/no se oculta correctamente
---

A menos que sea el primer tambor, debería tener un script `cuando se hace clic en la bandera`{:class="block3events"} para poderse `ocultar`{:class="block3looks"}. Y debería tener una secuencia de comandos `al recibir`{:class="block3events"} `este tambor` para `mostrar`{:class="block3looks"}.

Comprueba que el botón **Conseguir** para este tambor `envía`{:class="block3events"} el mismo mensaje.


--- /collapse ---

--- collapse ---
---
title: Mi botón Conseguir no aparece/no se oculta correctamente
---

A menos que el botón sea para el primer tambor, se debería `ocultar`{:class="block3looks"} `cuando se hace clic en la bandera`{:class="block3events"}. Y debería `aparecer`{:class="block3looks"} el mensaje `cuando recibo`{:class="block3events"} para el **tambor anterior**. El botón **Conseguir** debería `aparecer`{:class="block3looks"} para informar acerca de la próxima actualización que se viene.

--- /collapse ---

--- collapse ---
---
título: Puedo comprar un tambor cuando no tengo suficientes ritmos
---

Comprueba que hayas cambiado el número de `ritmos`{:class="block3variables"} necesarios `al hacer clic en este objeto`{:class="block3events"} en el del botón **Conseguir** para el tambor.

--- /collapse ---

--- collapse ---
---
title: El número de ritmos no cambia correctamente cuando consigo un tambor nuevo
---

Comprueba que hayas`cambiado ritmos en`{:class="block3variables"} un número negativo `al hacer clic en este objeto`{:class="block3events"} en el script del botón **Conseguir** para el tambor.

Asegúrate de que coincida con el número del disfraz del botón.

--- /collapse ---

--- /task ---

--- collapse ---
---
title: Proyecto terminado
---

Puedes ver el [proyecto terminado aquí](https://scratch.mit.edu/projects/522323676/){:target="_blank"}.

--- /collapse ---

**Consejo:** Si te confundes, no hay problema si eliminas el nuevo tambor y su botón y comienzas de nuevo. A veces es difícil detectar un error.

--- save ---
