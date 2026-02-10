
--- question ---

---
legend: Ερώτηση 2 από 3
---

Ένα έργο έχει αυτό το scriptγια να `ρωτήσει`{:class="block3sensing"} από τον χρήστη το όνομά του:

```blocks3
when flag clicked
set [name v] to [???] 
ask [What's your name?] and wait 
set [name v] to (answer)
```

![](images/q1-chatbot.png)

Ποια θα είναι η τιμή της μεταβλητής `όνομα`{:class="block3variables"} αφού ο παίκτης κάνει κλικ στο τικ (σημάδι ελέγχου) και τελειώσει το script;

--- choices ---

- ( ) όνομα

  --- feedback ---

Όχι, `name`{:class="block3variables"} ονομάζεται η μεταβλητή.

  --- /feedback ---

- ( ) ???

  --- feedback ---

Όχι, το `???` είναι η τιμή της μεταβλητής `όνομα`{:class="block3variables"} πριν από την εκτέλεση του μπλοκ `ρώτησε`{:class="block3sensing"}.

  --- /feedback ---

- ( ) απάντηση

  --- feedback ---

Όχι, `απάντηση`{:class="block3sensing"} είναι η ενσωματωμένη μεταβλητή που χρησιμοποιεί η Scratch για να αποθηκεύσει την απάντηση που πληκτρολογεί ένας χρήστης όταν `ρωτάς`{:class="block3sensing"} μια ερώτηση. --- /feedback ---

- (x) Μπόμπο

  --- feedback ---

Ναι, το μπλοκ`όρισε [name v] σε`{:class="block3variables"} ορίζει την **τιμή** της μεταβλητής `όνομα`{:class="block3variables"} στην τιμή `απάντηση`{:class= "block3sensing"} που είναι το κείμενο που εισήγαγε ο χρήστης.

Η τιμή `Μπόμπο` θα εμφανίζεται επίσης στη Σκηνή.

  --- /feedback ---

--- /choices ---

--- /question ---
