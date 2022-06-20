## Maak het speelveld

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In deze stap zet je het podium voor je eerste optreden en kies je een naam voor je rockster.
</div>
<div>
![](images/set-the-stage.png){:width="300px"}
</div>
</div>

--- task ---

Open het [Drum star starter project](https://scratch.mit.edu/projects/535783147/editor){:target="_blank"}. Scratch wordt in een nieuw browsertabblad geopend.

[[[working-offline]]]

--- /task ---

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
Muzikanten genaamd <span style="color: #0faeb0">**doe-het-zelf-artiesten**</span> beginnen muziek op te nemen vanuit hun slaapkamers. Ze produceren zelf hun eigen nummers en geven ze vervolgens online vrij zodat iedereen ze kan horen. 
</p>

Het spel begint in een slaapkamer als een doe-het-zelf-artiest.

--- task ---

Klik op **Kies een achtergrond** en zoek naar `bedroom`.

**Kies:** Selecteer een slaapkamer en voeg deze toe aan je project. We kozen `Bedroom 3`.

![Het podium met de achtergrond van 'Bedroom 3'.](images/bedroom3.png)

--- /task ---

--- task ---

In Scratch kun je code toevoegen aan het speelveld.

Klik op de achtergrond van je slaapkamer in het deelvenster Speelveld en voeg deze code toe:

![De background thumbnail in het deelvenster speelveld.](images/bedroom-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //de naam van je achtergrond
```

--- /task ---

Elke muzikant moet een rockster naam kiezen.

Een **variabele** is een manier om getallen en/of tekst op te slaan. Je rockstar-naam wordt opgeslagen in een `variabele`{:class="block3variables"} zodat deze op elk gewenst moment kan worden gebruikt.

--- task ---

Klik op het `Variabelen`{:class="block3variables"} blokkenmenu en selecteer de **Maak een variabele** knop.

Noem je nieuwe variabele `naam`:

![Het pop-upvenster nieuwe variabele met tekstinvoer 'naam'.](images/new-variable.png)

**Opmerking:** de nieuwe `naam` variabele verschijnt op het speelveld en kan nu worden gebruikt in de `variabele`{:class="block3variables"} blokken.

--- /task ---

--- task ---

Aan het begin van het project is de naam van je rockster onbekend.

Voeg een blok toe aan `Stel naam in op`{:class="block3variables"} `???`:

![](images/stage-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //de naam van je achtergrond
+ set [naam v] to [???] //jouw variabele
```

--- /task ---

Je kunt `een vraag stellen`{:class="block3sensing"} in Scratch en vervolgens een `variabele`{:class="block3variables"} gebruiken om het `antwoord`{:class="block3sensing"} op te slaan.

--- task ---

Klik op het blokken menu `Waarnemen`{:class="block3sensing"} en voeg een `Vraag`{:class="block3sensing"} blok toe aan je code:

![](images/stage-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //de naam van je achtergrond
set [naam v] to [???] //jouw variabele
+ ask [Wat is de naam van je rockstar?] and wait //je vraag
```

--- /task ---

--- task ---

Stel de `naam`{:class="block3variables"} `variabele`{:class="block3variables"} in op het `antwoord`{:class="block3sensing"}:

![](images/stage-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //de naam van je achtergrond
set [naam v] to [???] //jouw variabele
ask [Wat is de naam van je rockstar?] and wait //je vraag
+ set [naam v] to (answer)
```

--- /task ---

Verander de manier hoe je `variabele`{:class="block3variables"} op het podium eruit ziet.

--- task ---

Klik met de rechtermuisknop op de `variabele`{:class="block3variables"} op het podium en kies **groot uitlezen**:

![](images/large-readout.png)

--- /task ---

--- task ---

Sleep je `variabele`{:class="block3variables"} om deze in de rechterbovenhoek van het speelveld te plaatsen:

![](images/repositioned-variable.png)

--- /task ---

--- task ---

**Test:** Voer je project uit om ervoor te zorgen dat de `variabele`{:class="block3variables"} begint als `???` en vervolgens wordt bijgewerkt naar je `antwoord`{:class="block3sensing"}.

--- /task ---

--- task ---

Nu je hebt getest dat de `variabele`{:class="block3variables"} verandert in het `antwoord`{:class="block3sensing"}, kun je de laatste 2 blokken code wegslepen van de rest van het script. Dit betekent dat je geen `antwoord`{:class="block3sensing"} hoeft in te voeren telkens wanneer je je project test:

![](images/stage-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //de naam van je achtergrond
set [naam v] to [???] //jouw variabele
```

```blocks3
ask [Wat is de naam van je rockstar?] and wait //je vraag
set [naam v] to (answer)
```

--- /task ---

--- save ---
