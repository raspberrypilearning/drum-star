## Επίλεξε το Σκηνικό

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Σε αυτό το βήμα, θα δημιουργήσεις τη σκηνή για την πρώτη σου συναυλία και θα επιλέξεις ένα όνομα ροκ σταρ.
</div>
<div>
![](images/set-the-stage.png){:width="300px"}
</div>
</div>

--- task ---

Άνοιξε το αρχικό έργο [Ένα αστέρι στα τύμπανα](https://scratch.mit.edu/projects/535783147/editor){:target="_blank"}. Το Scratch θα ανοίξει σε νέα καρτέλα του φυλλομετρητή.

--- /task ---

The drummer starts in a bedroom like a beginner!

--- task ---

Κάνε κλικ στο **Επιλέξτε Υπόβαθρο** και αναζήτησε `υπνοδωμάτιο (bedroom)`.

Select a bedroom and add it to your project. Επιλέξαμε `Bedroom 3`.

![Η σκηνή που δείχνει το υπόβαθρο "Bedroom 3".](images/bedroom3.png)

--- /task ---

Στο Scratch, μπορείς να προσθέσεις κώδικα στο Υπόβαθρο.

--- task ---

Κάνε κλικ στο σκηνικό του υπνοδωματίου σου από το παράθυρο της Σκηνής και πρόσθεσε αυτόν τον κώδικα:

![Η μικρογραφία του υπόβαθρου στο παράθυρο σκηνής.](images/bedroom-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //your backdrop name
```

--- /task ---

Κάθε μουσικός πρέπει να επιλέξει ένα όνομα ροκ σταρ.

Μια **μεταβλητή** είναι ένας τρόπος αποθήκευσης αριθμών ή/και κειμένου. Το όνομά του ροκ σταρ σου, θα αποθηκευτεί σε μια `μεταβλητή`{:class="block3variables"}, ώστε να μπορεί να χρησιμοποιηθεί ανά πάσα στιγμή.

--- task ---

Από το μενού μπλοκ `Μεταβλητές`{:class="block3variables"} κάνε κλικ στο κουμπί **Δημιουργία μεταβλητής**.

Κάλεσε τη νέα σου μεταβλητή `όνομα`:

![Το αναδυόμενο παράθυρο Νέα μεταβλητή με εισαγωγή κειμένου «όνομα».](images/new-variable.png)

**Σημείωση:** Η νέα μεταβλητή `όνομα` εμφανίζεται στη Σκηνή και μπορεί πλέον να χρησιμοποιηθεί στα μπλοκ `Μεταβλητές`{:class="block3variables"}.

--- /task ---

--- task ---

Στην αρχή του έργου, το όνομα του ροκ σταρ σου είναι άγνωστο.

Πρόσθεσε ένα μπλοκ στο `όρισε όνομα σε`{:class="block3variables"} `???`:

![](images/stage-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //your backdrop name
+ set [name v] to [???] //your variable
```

--- /task ---

Μπορείς να προσθέσεις ένα μπλοκ`ρώτησε`{:class="block3sensing"} στο Scratch και μετά να χρησιμοποιήσεις μια `μεταβλητή`{:class="block3variables"} για να αποθηκεύσεις τις `απαντήσεις`{:class="block3sensing"}.

--- task ---

Κάνε κλικ στο μενού μπλοκ `Αισθητήρες`{:class="block3sensing"} και πρόσθεσε ένα μπλοκ `ρώτησε`{:class="block3sensing"} στον κώδικά σου:

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //your backdrop name
set [name v] to [???] //your variable
+ ask [What's your rock star name?] and wait //your question
```

--- /task ---

--- task ---

Όρισε τη `μεταβλητή`{:class="block3variables"} `όνομα`{:class="block3variables"} ως την `απάντηση`{:class="block3sensing"}:

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //your backdrop name
set [name v] to [???] //your variable
ask [What's your rock star name?] and wait //your question
+ set [name v] to (answer)
```

--- /task ---

--- task ---

Κάνε δεξί κλικ ξανά στη `μεταβλητή`{:class="block3variables"} που εμφανίζεται στη Σκηνή και επίλεξε **αλλαγή εύρους γραμμής κύλισης**:

![](images/large-readout.png)

--- /task ---

--- task ---

Drag your `variable`{:class="block3variables"} to position it top-right of the Stage:

![](images/repositioned-variable.png)

--- /task ---

--- task ---

**Δοκιμή:** Εκτέλεσε το έργο σου για να βεβαιωθείς ότι η `μεταβλητή`{:class="block3variables"} ξεκινά ως `???` και στη συνέχεια ενημερώνεται με την τιμή της `απάντησης`{:class="block3sensing"}.

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
