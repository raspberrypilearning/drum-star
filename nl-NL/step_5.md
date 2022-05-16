## Tweede upgrade

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Your drum skills are improving. Tijd voor een tweede upgrade! In deze stap kies je welke drum je wilt toevoegen.
</div>
<div>
![The Stage showing party backdrop with 3 drums.](images/second-upgrade.png){:width="300px"}
</div>
</div>

--- task ---

Duplicate the **Drum-snare** sprite:

![](images/duplicate-snare-drum.png)

--- /task ---

The **Drum Costumes** sprite has lots of drum costumes for you to choose from.

--- task ---

Click on the **Drum Costumes** sprite and select the **Costumes** tab.

**Choose:** a drum for the next upgrade. We kozen voor **Conga**.

Sleep de 'geraakt'- en 'niet geraakt'-uiterlijken van de door jou gekozen drum naar je nieuwe **Drum-snare2** sprite:

![Geanimeerde afbeelding die laat zien hoe je uiterlijken van de ene sprite naar de andere sleept.](images/drag-costumes.gif)

![The paint editor of the new sprite with two additional costumes in the costumes list.](images/drum-3-costumes.png)

--- /task ---

--- task ---

Name your drum to match the costumes you chose.

![](images/drum-3-named.png)

--- /task ---

--- task ---

Klik op het **Code** tabblad. Wijzig de code om de juiste uiterlijken te gebruiken en kies een geluid voor je nieuwe drum.

Change the number of beats you earn by clicking the new drum to `5`:

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

Drag your new drum into position on the Stage:

![New drum to the right of the other drums.](images/drum-3-positioned.png)

--- /task ---

Next, you need a button so that players can upgrade to this new drum.

--- task ---

Duplicate the **Get snare** sprite.

Position it in the bottom-right corner of the Stage. Change its name to `Get` and then the name of your new drum:

![The Sprite list with duplicated 'Get snare' sprite. The sprite name changed to match the new drum and positioned in the bottom-right of the Stage.](images/get-drum-3.png)

--- /task ---

--- task ---

Delete the **snare drum** from the button costume. Copy and paste the 'not hit' costume for your new drum to the button costume.

Click on the **Text** tool and change the number to `30` to show the cost of the new drum.

Your button should look like this:

![The paint editor showing the new button costume with chosen drum image and text updated to 30.](images/get-drum-copy.png)

--- /task ---


This button should `hide`{:class="block3looks"} at the start, then `show`{:class="block3looks"} when the player upgrades to the snare drum, so they know which drum they are working towards.

--- task ---

![](images/get-drum-3-icon.png)

```blocks3
when flag clicked
- show
+ hide
```

**Tip:** To delete a block, drag it to the Blocks menu, or right-click and choose **Delete Block**. Op een computer kun je ook op een blok klikken en vervolgens op <kbd>Delete</kbd> tikken om een blok te verwijderen.

--- /task ---

--- task ---

Add a `when I recieve`{:class="block3events"} script that your new drum button will show as the next upgrade when the player gets the **Drum-snare** drum:

![](images/get-drum-3-icon.png)

```blocks3
when I receive [snare v] // appear when previous drum is bought
show // show button for next available drum
```

--- /task ---

--- task ---

Wijzig het aantal slagen dat nodig is om deze drum te kopen, en het aantal slagen dat wordt verwijderd wanneer de speler deze drum krijgt.

Also change the message that is `broadcast`{:class="block3events"} when the player gets the new drum. Maak een nieuw bericht met de naam van je nieuwe drum:

![](images/get-drum-3-icon.png)

```blocks3
when this sprite clicked
if <(beats)>  [29]> then // change to 29
hide
change [beats v] by [-30] // change to 30
broadcast [conga v] // change to your drum name
else
say [Not enough beats!] for [2] seconds 
end
```

--- /task ---

--- task ---

Change the `when I receive snare`{:class="block3events"} script to `broadcast`{:class="block3events"} the name of your new drum. The drum will `show`{:class="block3looks"} when the player upgrades to the new drum:

![](images/drum-3-icon.png)

```blocks3
when I receive [conga v] // change to your drum name
show
```

--- /task ---

--- task ---

Voeg de **Feest** achtergrond toe.

Add a script to the Stage to switch the backdrop when the player upgrades to the new drum:

![](images/stage-icon.png)

```blocks3
when I receive [conga v] // change to your drum name
switch backdrop to (Party v)
```

--- /task ---

--- task ---

**Test:** Klik op de groene vlag om het spel te starten en test dat je genoeg slagen kunt verdienen om je nieuwe trommel te krijgen.

Wat gebeurt er als je op de knop klikt voordat je genoeg slagen hebt verdiend?

--- /task ---

--- save ---
