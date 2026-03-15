## Starttrommel

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Je voegt een **cymbal** sprite toe waarop je kunt klikken om beats te verdienen en een geluid te spelen.
</div>
<div>
![](images/starter-drum.png){:width="300px"}
</div>
</div>

--- task ---

Click **Choose a Sprite** and search `cymbal`.

![](images/cymbal-gallery.png)

--- /task ---

--- task ---

Add the **Drum-cymbal** sprite and position it on the Stage:

![](images/cymbal-stage.png)

--- /task ---

--- task ---

Voeg de **Muziek-extensie** toe:

[[[generic-scratch3-add-music-extension]]]

--- /task ---

--- task ---

Voeg een script toe om het cymbal een `ander uiterlijk`{:class="block3looks"} te geven en `speel een trommelgeluid`{:class="block3extensions"}:

![](images/cymbal-icon.png)

```blocks3
when this sprite clicked
switch costume to [drum-cymbal-b v] // hit costume
play drum [(5) Open High-Hat v] for [0.25] beats // drum sound
switch costume to [drum-cymbal-a v]  // not hit costume
```

--- /task ---

--- task ---

**Test:** Test je bekkens door erop te klikken.

You should hear a sound and see the costume change.

--- /task ---

Iedere keer dat je klikt op de **drum-cymbal** sprite verdien je één slag.

--- task ---

Create a `variable`{:class="block3variables"} (for all sprites) called `beats`:

![](images/beats-variable.png)

--- /task ---

--- task ---

Voeg een blok toe aan `verander slagen met 1`{:class="block3variables"} wanneer op de **Drum-cymbal** sprite wordt geklikt:

```blocks3
when this sprite clicked
+change [beats v] by [1]
switch costume to [drum-cymbal-b v]
play drum [(5) Open High-Hat v] for [0.25] beats 
switch costume to [drum-cymbal-a v]
```

--- /task ---

--- task ---

**Test:** Test the **Drum-cymbal** by clicking on it.

You should see the `beats`{:class="block3variables"} increase.

--- /task ---

De `slagen`{:class="block3variables"} variabele moet beginnen bij `0` slagen wanneer je een nieuw spel start.

--- task ---

Click on the Stage pane and then the **Code** tab.

Voeg een blok toe aan `zet slagen op`{:class="block3variables"} `0`:

![](images/stage-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) 
set [name v] to [???] 
+ set [beats v] to [0]
```
--- /task ---

--- task ---

**Test:** Klik op de groene vlag en zorg ervoor dat je `slagen`{:class="block3variables"} variabele begint op `0`.

--- /task ---

--- save ---
