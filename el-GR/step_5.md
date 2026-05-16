## More drums!

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Σε αυτό το βήμα, θα επιλέξεις ποιο τύμπανο θα προσθέσεις.
</div>
<div>
![Η σκηνή δείχνει σκηνικό πάρτι με 3 τύμπανα.](images/second-upgrade.png){:width="300px"}
</div>
</div>

--- task ---

Διπλασίασε το αντικείμενο **Drum-snare**:

![](images/duplicate-snare-drum.png)

--- /task ---

--- task ---

Κάνε κλικ στο αντικείμενο **Ενδυμασίες Τυμπάνων** και επίλεξε την καρτέλα **Ενδυμασίες**.

**Choose:** which drum to unlock next. Επιλέξαμε **Κόνγκα (Conga)**.


--- /task ---

--- task ---

Σύρε τις ενδυμασίες «χτυπημένο» και «μη χτυπημένο» του τυμπάνου που έχεις επιλέξει στο νέο σου αντικείμενο **Drum-snare2**:

![Κινούμενη εικόνα που δείχνει πώς να σύρεις τις ενδυμασίες από το ένα αντικείμενο στο άλλο.](images/drag-costumes.gif)

![Ο επεξεργαστής ζωγραφικής χρωμάτων του νέου αντικειμένου με δύο επιπλέον ενδυμασίες στη λίστα ενδυμασίων.](images/drum-3-costumes.png)

--- /task ---

--- task ---

Name the new drum to match the costumes you chose.

![](images/drum-3-named.png)

--- /task ---

--- task ---

Κάνε κλικ στην καρτέλα **Κώδικας**. Άλλαξε τον κώδικα για να χρησιμοποιήσεις τις σωστές ενδυμασίες και επίλεξε έναν ήχο για το νέο του τύμπανο.

Άλλαξε τον αριθμό των χτυπημάτων που κερδίζεις κάνοντας κλικ στο νέο τύμπανο σε `5`:

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

Σύρε το νέο σου τύμπανο στη θέση του στη Σκηνή:

![Νέο τύμπανο στα δεξιά των άλλων τυμπάνων.](images/drum-3-positioned.png)

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

Κάνε κλικ στο εργαλείο **Κείμενο** και άλλαξε τον αριθμό σε `30` για να εμφανίσεις το κόστος του νέου τυμπάνου.

![Ο επεξεργαστής ζωγραφικής δείχνει την νέα ενδυμασία του κουμπιού με την εικόνα του επιλεγμένου τυμπάνου και το κείμενο ενημερωμένο σε 30.](images/get-drum-copy.png)

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

Πρόσθεσε το σκηνικό **Party**.

--- /task ---

--- task ---

Πρόσθεσε ένα σενάριο στην Σκηνή για να αλλάξεις το υπόβαθρο όταν ο παίκτης αναβαθμιστεί στο νέο τύμπανο:

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
