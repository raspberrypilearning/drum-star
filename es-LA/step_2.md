## Prepara el escenario

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
En este paso, prepararás el escenario para tu primer concierto y elegirás tu nombre de estrella de rock.
</div>
<div>
![](images/set-the-stage.png){:width="300px"}
</div>
</div>

--- task ---

Abre el [proyecto inicial de Estrella de la batería](https://scratch.mit.edu/projects/535783147/editor){:target="_blank"}. Scratch se abrirá en otra pestaña del navegador.

--- /task ---

The drummer starts in a bedroom like a beginner!

--- task ---

Haz clic en **Elegir un Fondo** y busca `Bedroom`.

Select a bedroom and add it to your project. Elegimos `Bedroom 3`.

![El escenario muestra el telón de fondo 'Bedroom 3'.](images/bedroom3.png)

--- /task ---

En Scratch, puede agregar código a Stage (el escenario).

--- task ---

Haz clic en el fondo de tu dormitorio desde el panel Stage (Escenario) y agrega este código:

![La miniatura de fondo en el panel de escenario.](images/bedroom-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //your backdrop name
```

--- /task ---

Todo músico necesita elegir su nombre de estrella de rock.

Una **variable ** es una forma de almacenar números y/o texto. Tu nombre de estrella de rock se almacenará en una `variable `{:class="block3variables"} para ser utilizado en cualquier momento.

--- task ---

Haz clic en el menú de bloques `Variables`{:class="block3variables"} y selecciona el botón **Crear una Variable**.

Asígnale un `nombre`:

![La ventana emergente Nueva Variable con la entrada de texto 'nombre'.](images/new-variable.png)

**Aviso:** La nueva variable `nombre` aparece en el escenario y se puede usar ahora en los bloques `Variable`{:class="block3variables"}.

--- /task ---

--- task ---

Al comienzo del proyecto, tu nombre de estrella de rock es desconocido.

Agrega un bloque para `establecer nombre a`{:class="block3variables"} `???`:

![](images/stage-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //your backdrop name
+ set [name v] to [???] //your variable
```

--- /task ---

Puedes `preguntar`{:class="block3sensing"} en Scratch, luego usar una `variable`{:class="block3variables"} para almacenar la `respuesta`{:class="block3sensing"}.

--- task ---

Haz clic en el menú de bloques `Sensores`{:class="block3sensing"} y agrega un bloque `preguntar`{:class="block3sensing"} a tu código:

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //your backdrop name
set [name v] to [???] //your variable
+ ask [What's your rock star name?] and wait //your question
```

--- /task ---

--- task ---

Establece la `variable`{:class="block3variables"} `nombre`{:class="block3variables"} para la `respuesta`{:class="block3sensing"}:

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //your backdrop name
set [name v] to [???] //your variable
ask [What's your rock star name?] and wait //your question
+ set [name v] to (answer)
```

--- /task ---

--- task ---

Haz clic con el botón derecho en la `variable `{:class="block3variables"} en el Escenario y elige **tamaño grande**:

![](images/large-readout.png)

--- /task ---

--- task ---

Drag your `variable`{:class="block3variables"} to position it top-right of the Stage:

![](images/repositioned-variable.png)

--- /task ---

--- task ---

**Prueba:** Ejecuta tu proyecto para asegurarte de que la `variable`{:class="block3variables"} comience como `???`, luego se actualiza en tu`respuesta`{:class="block3sensing"}.

--- /task ---

You don't want to type an answer every time you test your project.

--- task ---

Drag the last two blocks of code away from the rest of the script.

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //your backdrop name
set [name v] to [???] //your variable
```

```blocks3
ask [What's your rock star name?] and wait //your question
set [name v] to (answer)
```

--- /task ---

--- save ---
