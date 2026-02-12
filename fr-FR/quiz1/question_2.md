
--- question ---

---
legend: Question 2 of 3
---

Un projet comporte ce script pour `demander`{:class="block3sensing"} à l'utilisateur son nom :

```blocks3
when flag clicked
set [name v] to [???] 
ask [What's your name?] and wait 
set [name v] to (answer)
```

![](images/q1-chatbot.png)

Quelle sera la valeur de la variable `nom`{:class="block3variables"} une fois que le joueur aura cliqué sur la coche et que le script se terminera ?

--- choices ---

- ( ) nom

  --- feedback ---

Non, `nom`{:class="block3variables"} est le nom de la variable.

  --- /feedback ---

- ( ) ???

  --- feedback ---

Non, `???` est la valeur de la variable `nom`{:class="block3variables"} avant l'exécution du bloc `demander`{:class="block3sensing"}.

  --- /feedback ---

- ( ) réponse

  --- feedback ---

Non, `réponse`{:class="block3sensing"} est la variable intégrée que Scratch utilise pour stocker la réponse qu'un utilisateur tape lorsque tu `demandes`{:class="block3sensing"} une question. --- /feedback ---

- (x) Bobo

  --- feedback ---

Oui, le bloc `mettre [nom v] à`{:class="block3variables"} définit la **valeur** de la variable `nom`{:class="block3variables"} sur la valeur de `demande`{:class= "block3sensing"} qui est le texte saisi par l'utilisateur.

La valeur `Bobo` sera également affichée sur la Scène.

  --- /feedback ---

--- /choices ---

--- /question ---
