
--- question ---

---
legend: Pregunta 2 de 3
---

Un proyecto tiene esta secuencia de comandos para `preguntar`{:class="block3sensing"} al usuario por su nombre:

```blocks3
when flag clicked
set [nombre v] to [???] 
ask [¿Cómo te llamas?] and wait 
set [nombre v] to (answer)
```

![](images/q1-chatbot.png)

¿Cuál será el valor de la variable `nombre`{:class="block3variables"} después de que se hace clic en la marca de verificación y se finaliza la secuencia de comandos?

--- choices ---

- ( ) nombre

  --- feedback ---

No, el `nombre`{:class="block3variables"} es el nombre de la variable.

  --- /feedback ---

- ( ) ???

  --- feedback ---

No, `???` es el valor de la variable `nombre`{:class="block3variables"} antes de que se ejecute el bloque `preguntar`{:class="block3sensing"}.

  --- /feedback ---

- ( ) respuesta

  --- feedback ---

No, `respuesta`{:class="block3sensing"} es la variable integrada que utiliza Scratch para almacenar la respuesta que alguien escribe al `preguntar`{:class="block3sensing"}.
--- /feedback ---

- (x) Bobo

  --- feedback ---

Sí, el bloque `fijar [nombre v] a`{:class="block3variables"} establece el **valor** de la variable `nombre`{:class="block3variables"} en el valor de `respuesta`{:class="block3sensing"} que es el texto que se ingresó.

El valor `Bobo` también se mostrará en el Escenario.

  --- /feedback ---

--- /choices ---

--- /question ---
