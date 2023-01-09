## Gosod y Llwyfan

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Yn y cam yma, byddi di'n gosod y llwyfan ar gyfer dy gig cyntaf ac yn dewis enw seren roc.
</div>
<div>
![](images/set-the-stage.png){:width="300px"}
</div>
</div>

--- task ---

Agora'r [prosiect Seren ddrymiau](https://scratch.mit.edu/projects/535783147/editor){:target="_blank"}. Bydd Scratch yn agor mewn tab arall ar y porwr.

[[[working-offline]]]

--- /task ---

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
Mae cerddorion sy'n cael eu galw'n <span style="color: #0faeb0">**artistiaid DIY**</span> yn dechrau recordio cerddoriaeth o'u hystafelloedd gwely. Maen nhw'n cynhyrchu eu caneuon eu hunain ar eu pennau eu hunain ac yna'n eu rhyddhau ar-lein i bawb eu clywed. 
</p>

Mae'r gêm yn dechrau mewn ystafell wely fel artist DIY.

--- task ---

Clicia **Dewiswch Gefnlen** a chwilio am `bedroom`.

**Dewis:** Dewisa ystafell wely a'i hychwanegu at dy brosiect. Fe ddewison ni `Bedroom 3`.

![Y llwyfan yn dangos y gefnlen 'Bedroom 3'.](images/bedroom3.png)

--- /task ---

--- task ---

Yn Scratch, galli di ychwanegu cod at y Llwyfan.

Clicia ar dy gefnlen ystafell wely o gwarel y Llwyfan ac ychwanegu'r cod yma:

![Mân lun o'r gefnlen yng nghwarel y llwyfan.](images/bedroom-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //enw dy gefnlen
```

--- /task ---

Mae angen i bob cerddor ddewis enw seren roc.

Mae **newidyn** yn ffordd o storio rhifau a/neu destun. Bydd enw dy seren roc yn cael ei storio mewn `newidyn`{:class="block3variables"} fel bod modd ei ddefnyddio unrhyw bryd.

--- task ---

O'r ddewislen blociau `Newidynnau`{:class="block3variables"} clicia'r botwm **Creu Newidyn**.

Newidia enw dy newidyn i `enw`:

![Y ffenestr naid Newidyn Newdd gyda'r testun 'name'.](images/new-variable.png)

**Nodyn:** Bydd y newidyn `enw` newydd yn ymddangos ar y Llwyfan a bydd modd ei ddefnyddio nawr yn y blociau `Newidyn`{:class="block3variables"}.

--- /task ---

--- task ---

Ar ddechrau'r prosiect, mae enw dy seren roc yn anhysbys.

Ychwanega floc i `gosod enw i`{:class="block3variables"} `???`:

![](images/stage-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //enw dy gefnlen
+ set [enw v] to [???] //dy newidyn
```

--- /task ---

Galli di `ofyn`{:class="block3sensing"} cwestiwn yn Scratch, ac wedyn defnyddio `newidyn`{:class="block3variables"} i storio'r `ateb`{:class="block3sensing"}.

--- task ---

Clicia ar y ddewislen flociau `Synhwyro`{:class="block3sensing"} ac ychwanegu bloc `gofyn`{:class="block3sensing"} at dy god:

![](images/stage-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //enw dy gefnlen
set [enw v] to [???] //dy newidyn
+ ask [Beth yw enw dy seren roc?] and wait //dy gwestiwn
```

--- /task ---

--- task ---

Gosoda'r `newidyn`{:class="block3variables"} `enw`{:class="block3variables"} i'r `ateb`{:class="block3sensing"}:

![](images/stage-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //enw dy gefnlen
set [enw v] to [???] //dy newidyn
ask [Beth yw enw dy seren roc?] and wait //dy gwestiwn
+ set [enw v] to (answer)
```

--- /task ---

Newidia'r ffordd mae dy `newidyn`{:class="block3variables"} yn edrych ar y Llwyfan.

--- task ---

De-glicia ar y `newidyn`{:class="block3variables"} ar y Llwyfan a dewis **sgrîn fawr**:

![](images/large-readout.png)

--- /task ---

--- task ---

Llusga dy `newidyn`{:class="block3variables"} er mwyn ei leoli ar ochr dde uchaf y Llwyfan:

![](images/repositioned-variable.png)

--- /task ---

--- task ---

**Prawf:** Rheda dy brosiect i wneud yn siŵr bod y `newidyn`{:class="block3variables"} yn dechrau fel `???` ac wedyn yn diweddaru i dy `ateb`{:class="block3sensing"}.

--- /task ---

--- task ---

Nawr dy fod ti wedi profi i wneud yn siŵr bod y `newidyn`{:class="block3variables"} yn newid i'r `ateb`{:class="block3sensing"}, galli di lusgo'r 2 floc o god i ffwrdd o weddill y sgript. Mae hyn yn golygu nad oes rhaid i ti deipio `ateb`{:class="block3sensing"} bob tro rwyt ti'n profi dy brosiect:

![](images/stage-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //enw dy gefnlen
set [enw v] to [???] //dy newidyn
```

```blocks3
ask [Beth yw enw dy seren roc?] and wait //dy gwestiwn
set [enw v] to (answer)
```

--- /task ---

--- save ---
