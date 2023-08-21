## Πρώτη αναβάθμιση

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Θα προσθέσεις την πρώτη σου αναβάθμιση. Το κουμπί **Πάρε ταμπούρο** θα εμφανιστεί στην αρχή, ώστε ο παίκτης να ξέρει ποιο τύμπανο θέλει να αποκτήσει.
</div>
<div>
![](images/first-upgrade.png){:width="300px"}
</div>
</div>

--- task ---

Πρόσθεσε το αντικείμενο **Drum-snare** στο έργο σου και τοποθέτησε το στο Υπόβαθρο:

![](images/snare-stage.png)

--- /task ---

--- task ---

Σύρε το script `όταν γίνει κλικ σε αυτό το αντικείμενο`{:class="block3events"} από το αντικείμενο **Drum-cymbal** στο αντικείμενο **Drum-snare**.

[[[scratch3-copy-code]]]

--- /task ---

--- task ---

Άλλαξε τις ενδυμασίες και τον ήχο του τυμπάνου.

Άλλαξε τον αριθμό των χτυπημάτων που κερδίζεις σε `2`:

![](images/snare-icon.png)

```blocks3
when this sprite clicked
+change [beats v] by [2] //2 beats per click
+switch costume to [drum-snare-b v] //hit costume
+play drum [(1) Snare Drum v] for [0.25] beats //drum sound
+switch costume to [drum-snare-a v] //not hit costume
```

--- /task ---

--- task ---

**Δοκιμή:** Τρέξε το έργο σου. Βεβαιώσου ότι κερδίζεις 2 χτυπήματα όταν κάνεις κλικ στο ταμπούρο.

--- /task ---

Οι αναβαθμίσεις δεν είναι διαθέσιμες όταν ξεκινάς το έργο. Πρέπει να κερδίζονται με χτυπήματα.

--- task ---

Πρόσθεσε ένα script για να αποκρύψεις αυτό το αντικείμενο **τύμπανο** στην αρχή του έργου:

![](images/snare-icon.png)

```blocks3
when flag clicked
hide
```

--- /task ---

Ένα κουμπί θα δείξει ποιο τύμπανο είναι η επόμενη επιλογή αναβάθμισης και πόσα χτυπήματα θα κοστίσει.

--- task ---

**Διπλασίασε** το αντικείμενο **Πάρε**:

![](images/duplicate-get.png)

Άλλαξε την προβολή σε **Εμφάνιση** και άλλαξε το όνομά του σε `Πάρε ταμπούρο`. Τοποθέτησε το στην κάτω δεξιά γωνία της Σκηνής:

![](images/get-snare.png)

--- /task ---

--- task ---

Κάνε κλικ στο αντικείμενο **Drum-snare** και επίλεξε την καρτέλα **Ενδυμασίες**. Χρησιμοποιήσε το εργαλείο **Επιλογή** (βέλος) για να επισημάνεις τη μη χτυπημένη ενδυμασία του τυμπάνου σου. Κάνε κλικ στο εικονίδιο **Ομαδοποίηση** και στη συνέχεια στο εικονίδιο **Αντιγραφή**:

![](images/snare-icon.png)

![](images/copy-costume.png)

--- /task ---

--- task ---

Κάνε κλικ στο αντικείμενο **Get snare** και **Επιλόλλησε** στην ενδυμασία ταμπούρο. Ίσως χρειαστεί να αλλάξεις το μέγεθος και να το τοποθετήσεις κατάλληλα ώστε να ταιριάζει στο κουμπί σου:

![](images/get-snare-icon.png)

![](images/paste-costume.png)

--- /task ---

--- task ---

Κάνε κλικ στην καρτέλα **Κώδικας** και πρόσθεσε ένα σενάριο για να εμφανιστεί το αντικείμενο **Πάρε ταμπούρο** στην αρχή του έργου:

![](images/get-snare-icon.png)

```blocks3
when flag clicked
show
```

--- /task ---

Η αναβάθμιση μπορεί να αγοραστεί μόνο εάν ο χρήστης έχει `10` ή περισσότερα χτυπήματα. Στο [Grow a dragonfly](https://projects.raspberrypi.org/en/projects/grow-a-dragonfly){:target="_blank"}, έμαθες πώς να λαμβάνεις αποφάσεις με `εάν`{:class="block3control"} μπλοκ.

Ένα μπλοκ `εάν ... αλλιώς`{:class="block3control"} χρησιμοποιείται για τη λήψη μιας απόφασης και θα κάνει διαφορετικά πράγματα εάν μια συνθήκη είναι `αληθής` ή `ψευδής`.

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
Χρησιμοποιούμε <span style="color: #0faeb0">**αν ... αλλιώς**</span> όλη την ώρα για να λάβουμε αποφάσεις. Όταν ξυπνάς, ελέγχεις `εάν`{:class="block3control"} είναι πρωί. Σηκώνεσαι ή `αλλιώς`{:class="block3control"} κοιμάσαι ξανά. Μπορείς να σκεφτείς άλλες αποφάσεις «αν ... αλλιώς»{:class="block3control"} που λαμβάνεις; 
</p>

--- task ---

Add this code to get the upgrade `if`{:class="block3control"} the player has enough beats, or `say`{:class="block3looks"} `More beats needed!` if they are not able to upgrade:

![](images/get-snare-icon.png)

```blocks3
when this sprite clicked
if <(beats)>  [9]> then //if 10 or more beats
hide
change [beats v] by [-10] //take away the cost of upgrade
else
say [More beats needed!] for [2] seconds 
end
```

--- /task ---

Instead of only telling the player they need **more** beats, you can tell the player exactly **how many more** beats are needed to get the upgrade.

A `join`{:class="block3operators"} block is used to concatenate, or 'link' two values together.

![](images/get-snare-icon.png)

--- task ---

Add this code to `join`{:class="block3operators"} the number of beats needed with the text you have used to tell the player they need more beats if they are not able to upgrade:

```blocks3
when this sprite clicked
if <(beats)>  [9]> then //if 10 or more beats
hide
change [beats v] by [-10] //take away the cost of upgrade
else
+ say (join ((10) - (beats)) [beats needed!]) for [2] seconds
end
```

--- /task ---

--- task ---

Add a `broadcast`{:class="block3events"} block to send a new `snare` message:

![](images/get-snare-icon.png)

```blocks3
when this sprite clicked
if <(beats)>  [9]> then // if 10 or more beats
hide
change [beats v] by [-10] // take away the cost of upgrade
+ broadcast [snare v] // your drum name
else
say (join ((10) - (beats)) [beats needed!]) for [2] seconds
end
```

--- /task ---

--- task ---

Click on the **Drum-snare** sprite. Add this script:

![](images/snare-icon.png)

```blocks3
when I receive [snare v]
show
```

--- /task ---

When you upgrade your equipment, you will be able to play at bigger venues.

--- task ---

Add another backdrop. We chose **Chalkboard** to play our second gig at school.

Add code to the Stage to `switch backdrop`{:class="block3looks"} when the upgrade message is received:

![](images/stage-icon.png)

```blocks3
when I receive [snare v]
switch backdrop to [Chalkboard v]
```

**Tip:** Choose a venue that's a small step up from the bedroom. You want to save bigger venues for later.

--- /task ---

--- task ---

**Test:** Run your project. Try and buy the snare upgrade before you have enough beats.

When you buy the upgrade check: the snare appears, the button disappears, the venue changes and the `beats`{:class="block3variables"} go down by `10`.

--- /task ---

--- save ---
