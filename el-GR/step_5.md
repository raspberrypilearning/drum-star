## Δεύτερη αναβάθμιση

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Οι ικανότητές σου στα τύμπανα βελτιώνονται. Ώρα για δεύτερη αναβάθμιση! Σε αυτό το βήμα, θα επιλέξεις ποιο τύμπανο θα προσθέσεις.
</div>
<div>
![Η σκηνή δείχνει σκηνικό πάρτι με 3 τύμπανα.](images/second-upgrade.png){:width="300px"}
</div>
</div>

--- task ---

Διπλασίασε το αντικείμενο **Drum-snare**:

![](images/duplicate-snare-drum.png)

--- /task ---

Το αντικείμενο **Ενδυμασίες Τυμπάνων** έχει πολλές ενδυμασίες τυμπάνων από τις οποίες μπορείς να επιλέξεις.

--- task ---

Κάνε κλικ στο αντικείμενο **Ενδυμασίες Τυμπάνων** και επίλεξε την καρτέλα **Ενδυμασίες**.

**Επίλεξε:** ένα τύμπανο για την επόμενη αναβάθμιση. Επιλέξαμε **Κόνγκα (Conga)**.

Σύρε τις ενδυμασίες «χτυπημένο» και «μη χτυπημένο» του τυμπάνου που έχεις επιλέξει στο νέο σου αντικείμενο **Drum-snare2**:

![Κινούμενη εικόνα που δείχνει πώς να σύρεις τις ενδυμασίες από το ένα αντικείμενο στο άλλο.](images/drag-costumes.gif)

![Ο επεξεργαστής ζωγραφικής χρωμάτων του νέου αντικειμένου με δύο επιπλέον ενδυμασίες στη λίστα ενδυμασίων.](images/drum-3-costumes.png)

--- /task ---

--- task ---

Ονόμασε το τύμπανο σου ώστε να ταιριάζει με τις ενδυμασίες που επέλεξες.

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

Στη συνέχεια, χρειάζεσαι ένα κουμπί για να μπορούν οι παίκτες να κάνουν αναβάθμιση σε αυτό το νέο τύμπανο.

--- task ---

Αντίγραψε το αντικείμενο **Πάρε ταμπούρο**.

Τοποθέτησε το στην κάτω δεξιά γωνία του Σκηνικού. Άλλαξε το όνομά του σε `Πάρε` και μετά το όνομα του νέου σου τυμπάνου:

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

**Tip:** To delete a block, drag it to the Blocks menu, or right-click and choose **Delete Block**. On a computer, you can also click on a block and then tap <kbd>Delete</kbd> to remove a block.

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

Change the number of beats needed to buy this drum, and the number of beats that are removed, when the player gets this drum.

Also change the message that is `broadcast`{:class="block3events"} when the player gets the new drum. Create a new message with the name of your new drum:

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

Add the **Party** backdrop.

Add a script to the Stage to switch the backdrop when the player upgrades to the new drum:

![](images/stage-icon.png)

```blocks3
when I receive [conga v] // change to your drum name
switch backdrop to (Party v)
```

--- /task ---

--- task ---

**Test:** Click the green flag to start the game and test that you can earn enough beats to get your new drum.

What happens if you click the button before you have earned enough beats?

--- /task ---

--- save ---
