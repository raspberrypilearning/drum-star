
--- question ---

---
legend: Pregunta 3 de 3
---

Usaste esta secuencia de comandos para controlar lo que sucede cuando se hace clic en el botón para actualizar el tambor:

```blocks3
when this sprite clicked
if <(ritmos)>  [29]> then 
hide
change [ritmos v] by [-30] 
broadcast (conga v) 
else
say [¡No hay suficientes ritmos!] for [2] seconds 
end
```

Si el valor de la variable `ritmos`{:class="block3variables"} es `29`, ¿qué sucederá cuando alguien haga clic en el botón?

--- choices ---

- ( ) El objeto se va a `ocultar`{:class="block3looks"}

  --- feedback ---

  No del todo, hay un bloque `ocultar`{:class="block3looks"} en la secuencia de comandos, pero no se ejecutará con `29` `ritmos`{:class="block3variables"}. Echa un vistazo a la secuencia de comandos de nuevo.

  --- /feedback ---

- (x) El objeto botón va a `decir`{:class="block3looks"} `¡No hay suficientes ritmos!`

  --- feedback ---

Sí, la condición comprueba si los `ritmos`{:class="block3variables"} son mayores a `29`, pero los `ritmos`{:class="block3variables"} son iguales a `29`, por lo que no se tiene lo suficiente.

  --- /feedback ---

- ( ) Se restarán 30 al valor de la variable `ritmos`{:class="block3variables"}

  --- feedback ---

  No, el valor de la variable `ritmos`{:class="block3variables"} seguirá siendo el mismo. `ritmos`{:class="block3variables"} es `29` lo que significa que `ritmos`{:class="block3variables"} `> 29` es falso, por lo que la primera parte del bloque `si`{:class El bloque ="block3control"} no se ejecutará.

  --- /feedback ---

- ( ) Nada

  --- feedback ---

  No, la secuencia de comandos siempre producirá algo. Echale un vistazo más de cerca para ver qué parte de la secuencia de comandos se ejecutará cuando tengas `29` `ritmos`{:class="block3variables"}.

  --- /feedback ---

--- /choices ---

--- /question ---
