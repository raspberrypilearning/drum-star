
--- question ---

---
legend: Question 3 sur 3
---

Tu as utilisé ce script pour contrôler ce qui se passe lorsque le joueur clique sur le bouton pour améliorer son tambour :

```blocks3
when this sprite clicked
if <(battements)>  [29]> then 
hide
change [battements v] by [-30] 
broadcast (conga v) 
else
say [Pas assez de battements !] for [2] seconds 
end
```

Si la valeur de la variable `battements`{:class="block3variables"} est `29`, que se passera-t-il lorsque le joueur cliquera sur le bouton ?

--- choices ---

- ( ) Le sprite sera `caché`{:class="block3looks"}

  --- feedback ---

  Pas tout à fait, il y a un bloc `cacher`{:class="block3looks"} dans le script, mais il ne fonctionnera pas avec `29` `battements`{:class="block3variables"}. Jette à nouveau un coup d'œil au script.

  --- /feedback ---

- (x) Le sprite du bouton `dira`{:class="block3looks"} `Pas assez de battements !`

  --- feedback ---

Oui, la condition vérifie si `battements`{:class="block3variables"} est supérieur à `29`, mais `battements`{:class="block3variables"} est égal à `29` donc le joueur n'en a pas assez.

  --- /feedback ---

- ( ) 30 sera retiré de la valeur de la variable `battements`{:class="block3variables"}

  --- feedback ---

  Non, la valeur de la variable `battements`{:class="block3variables"} restera la même. `battements`{:class="block3variables"} est à `29` ce qui signifie que `battements`{:class="block3variables"} `> 29` est faux, donc les blocs dans la première partie du bloc `si`{:class="block3control"} ne s'exécuteront pas.

  --- /feedback ---

- ( ) Rien

  --- feedback ---

  Non, le script fera toujours quelque chose. Regarde de plus près pour voir quelle partie du script s'exécutera lorsque tu auras `29` `battements`{:class="block3variables"}.

  --- /feedback ---

--- /choices ---

--- /question ---
