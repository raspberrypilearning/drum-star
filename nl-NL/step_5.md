## More drums!

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In deze stap kies je welke drum je wilt toevoegen.
</div>
<div>
![het speelveld met de achtergrond van een feestje met 3 drums.](images/second-upgrade.png){:width="300px"}
</div>
</div>

--- task ---

Dupliceer de **Drum-snare** sprite:

![](images/duplicate-snare-drum.png)

--- /task ---

--- task ---

Klik op de **Drum Uiterlijken** sprite en selecteer het tabblad **Uiterlijken**.

**Choose:** which drum to unlock next. We kozen voor **Conga**.


--- /task ---

--- task ---

Sleep de 'geraakt'- en 'niet geraakt'-uiterlijken van de door jou gekozen drum naar je nieuwe **Drum-snare2** sprite:

![Geanimeerde afbeelding die laat zien hoe je uiterlijken van de ene sprite naar de andere sleept.](images/drag-costumes.gif)

![De verf editor van de nieuwe sprite met twee extra uiterlijken in de uiterlijkenlijst.](images/drum-3-costumes.png)

--- /task ---

--- task ---

Name the new drum to match the costumes you chose.

![](images/drum-3-named.png)

--- /task ---

--- task ---

Klik op het **Code** tabblad. Wijzig de code om de juiste uiterlijken te gebruiken en kies een geluid voor je nieuwe drum.

Wijzig het aantal slagen dat je verdient door op de nieuwe drum te klikken in `5`:

![](images/drum-3-icon.png)

```blocks3
when this sprite clicked
+change [beats v] by [5] //5 beats per click
+switch costume to [ v] //your hit costume
+play drum [ v] for [0.25] beats //your drum sound
+switch costume to [ v] //your not hit costume
```

--- /task ---

--- task ---

Sleep je nieuwe drum naar de juiste positie op het speelveld:

![Nieuwe drum rechts van de andere drums.](images/drum-3-positioned.png)

--- /task ---

Add a button so that players can unlock the new drum.

--- task ---

Duplicate the **Get snare** sprite and position it in the bottom-right corner of the Stage.

--- /task ---

--- task ---

Change its name (for example `Get conga`):

![The Sprite list with duplicated 'Get snare' sprite. The sprite name has been changed to match the new drum type and positioned in the bottom-right of the Stage.](images/get-drum-3.png)

--- /task ---

--- task ---

Delete the **snare drum** from the new 'Get' button costume.

--- /task ---

--- task ---

Copy the 'not hit' costume for your new drum and paste it to the new 'Get' button costume.

--- /task ---

--- task ---

Klik op de **Tekst** tool en wijzig het getal in `30` om de kosten van de nieuwe drum weer te geven.

![De Paint editor toont het nieuwe uiterlijk van de knop met de gekozen drumafbeelding en de tekst bijgewerkt naar 30.](images/get-drum-copy.png)

--- /task ---

Your new 'Get' button should `hide`{:class="block3looks"} at the start.

--- task ---

![](images/get-drum-3-icon.png)

```blocks3
when flag clicked
+ hide
```

--- /task ---

--- task ---

Add a `when I receive`{:class="block3events"} script that your new 'Get' button will `show`{:class="block3looks"} when the player unlocks the snare drum.

```blocks3
when I receive [snare v] // appear when previous drum is unlocked
show // show button to get the new drum
```

--- /task ---

--- task ---

Change:
- The number of beats needed to unlock this drum
- The number of beats that are removed when the player unlocks this drum.
- The message that is `broadcast`{:class="block3events"} when the player gets the new drum.

```blocks3
when this sprite clicked
if <(beats)>  [29]> then // change to 29
hide
change [beats v] by [-30] // change to -30
broadcast (conga v) // change to your drum name
else
say [More beats needed!] for [2] seconds 
end
```

--- /task ---

--- task ---

Click your new drum sprite and change the `when I receive snare`{:class="block3events"} script to show it when your new drum is unlocked:

```blocks3
when I receive [conga v] // change to your drum name
show
```

--- /task ---

--- task ---

Voeg de **Feest** achtergrond toe.

--- /task ---

--- task ---

Voeg een script toe aan het speelveld om de achtergrond te veranderen wanneer de speler een upgrade uitvoert naar de nieuwe drum:

![](images/stage-icon.png)

```blocks3
when I receive [conga v] // change to your drum name
switch backdrop to (Party v)
```

--- /task ---

--- task ---

**Test:** Click the green flag to start the game.

You should unlock your new drum if you earn enough beats.

What happens if you click the button before you have earned enough beats?

--- /task ---

--- save ---
