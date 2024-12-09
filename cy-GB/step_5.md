## More drums!

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Yn y cam yma, byddi di'n yn dewis pa ddrwm i'w ychwanegu.
</div>
<div>
![Y Llwyfan yn dangos golygfa o barti gyda thri drwm.](images/second-upgrade.png){:width="300px"}
</div>
</div>

--- task ---

Dyblyga'r corlun **Drum-snare**:

![](images/duplicate-snare-drum.png)

--- /task ---

--- task ---

Clicia'r corlun **Drum Costumes** ac wedyn mynd i'r tab **Gwisgoedd**.

**Choose:** which drum to unlock next. Fe ddewison ni **Conga**.


--- /task ---

--- task ---

Llusga'r gwisgoedd 'hit' a 'not hit' o'r drwm y gwnes di ei ddewis i dy gorlun **Drum-snare2** newydd:

![Delwedd animeiddiedig yn dangos sut i lusgo gwisgoedd o un corlun i'r llall.](images/drag-costumes.gif)

![Golygydd paent y corlun newydd gyda dwy wisg ychwanegol yn y rhestr gwisgoedd.](images/drum-3-costumes.png)

--- /task ---

--- task ---

Name the new drum to match the costumes you chose.

![](images/drum-3-named.png)

--- /task ---

--- task ---

Clicia'r tab **Cod**. Newidia'r cod i ddefnyddio'r gwisgoedd cywir a dewis sain ar gyfer dy ddrwm newydd.

Newidia nifer y curiadau rwyt ti'n eu hennill drwy glicio'r drwm newydd i `5`:

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

Llusga dy ddrwm newydd i'w le ar y Llwyfan:

![Drwm newydd i'r dde o'r drymiau eraill.](images/drum-3-positioned.png)

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

Clicia'r offeryn **Text** a newid y rhif i `30` i ddangos cost y drwm newydd.

![Y golygydd paent yn dangos gwisg newydd y botwm gyda delwedd y drwm a ddewiswyd a'r testun wedi'i ddiweddaru i 30.](images/get-drum-copy.png)

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

Ychwanega'r gefnlen **Party**.

--- /task ---

--- task ---

Ychwanega sgript i'r Llwyfan i newid y gefnlen pan fydd y chwaraewr yn uwchraddio i'r drwm newydd:

![](images/stage-icon.png)

```blocks3
when I receive [conga v] // change to your drum name
switch backdrop to (Party v)
```

--- /task ---

--- task ---

**Test:** Click the green flag to start the game.

You should get unlock your new drum if you earn enough beats.

What happens if you click the button before you have earned enough beats?

--- /task ---

--- save ---
