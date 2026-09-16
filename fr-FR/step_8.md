## Défi

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Améliore ton projet avec plus de tambours et plus de décors à mesure que tu joues dans des salles plus prestigieuses. 
</div>
<div>
![](images/upgrade-project.png){:width="300px"}
</div>
</div>

### Ajouter plus de tambours

Pour ajouter un autre tambour à déverrouiller, reporte-toi aux étapes précédentes du projet.

Voici quelques rappels si tu en as besoin.

--- collapse ---

---
title: Pour le tambour
---

--- task ---

Duplique le précédent sprite **tambour** et ajoute deux costumes.

--- /task ---

--- task ---

Modifie le `costume`{:class="block3looks"} et le `son`{:class="block3sound"} utilisés dans le script `Quand ce sprite est cliqué`{:class="block3events"}.

--- /task ---

--- task ---

Modifie le nombre de `battements`{:class="block3variables"} gagnés dans le script `quand ce sprite est cliqué`{:class="block3events"}.

--- /task ---

--- task ---

Change le `message`{:class="block3events"} qui fait que le tambour `montre`{:class="block3looks"} un message pour le **nouveau tambour**.

--- /task ---

--- /collapse ---

--- collapse ---

---
title: Pour le bouton « avoir »
---

--- task ---

Duplique le précédent sprite **avoir**.

--- /task ---

--- task ---

Change le `message`{:class="block3events"} qui fait apparaître le bouton au `message`{:class="block3events"} `diffusé`{:class="block3events"} par le **tambour précédent**.

--- /task ---

--- task ---

Change le `costume`{:class="block3looks"} ainsi que le coût du nouveau tambour.

--- /task ---

--- task ---

Modifie le nombre de `battements`{:class="block3variables"} que tu dois avoir pour déverrouiller ce tambour dans la condition `si`{:class="block3events"}. Change le nombre négatif de `battements`{:class="block3variables"} que tu `mets`{:class="block3variables"} lorsque tu obtiens ce tambour. Modifie le nombre de `battements`{:class="block3variables"} qui doit être soustrait dans le bloc `regrouper`{:class="block3operators"}. Remplace le message qui est `envoyé à tous`{:class="block3events"} par le nom du **nouveau tambour**.

--- /task ---

--- /collapse ---

--- collapse ---

---
title: Pour la salle
---

--- task ---

Ajoute un nouvel arrière-plan.

--- /task ---

--- task ---

Ajoute un script à la scène pour `basculer sur l'arrière-plan`{:class="block3looks"} sur le nouveau arrière-plan lorsque le `message`{:class="block3events"} pour ce tambour est reçu.

--- /task ---

Tu constateras peut-être que tes tambours doivent être dans une nouvelle position sur un arrière-plan différent.

--- task ---

Ajoute un script commençant par `quand l'arrière-plan bascule sur`{:class="block3events"} à chaque sprite **tambour** avec un bloc `aller à`{:class="block3motion"} pour les faire changer de position.

Tu devras également définir leur position de départ `quand le drapeau est cliqué`{:class="block3events"}.

--- /task ---

--- /collapse ---

### Améliorer le retour au joueur

Indique au joueur exactement **combien de** battements supplémentaires sont nécessaires pour débloquer le tambour suivant.

--- task ---

Ajoute ce code pour `regrouper`{:class="block3operators"} le nombre de battements nécessaires avec le texte que tu as utilisé pour indiquer au joueur qu'il lui faut plus de battements s'il n'en a pas assez pour débloquer le tambour suivant :

```blocks3
when this sprite clicked
if <(beats)>  [9]> then //if 10 or more beats
hide
change [beats v] by [-10] //take away the cost of upgrade
else
+ say (join ((10) - (beats)) [beats needed!]) for [2] seconds
end
```

**Remarque** : mets à jour les nombres pour qu’ils correspondent à ceux nécessaires pour débloquer chaque tambour.

--- /task ---

### Nettoyer ton code

--- task ---

**Bien organisé :** si tu as le temps, alors c'est une bonne idée de t'assurer que les sprites dans la liste des sprites sont dans un ordre raisonnable, en commençant par les tambours dans leur ordre verrouillé, puis les boutons dans l'ordre.

--- /task ---

--- task ---

### Besoin d’aide ?

**Débogage :** assure-toi d'abord que tu comprends vraiment quand le tambour et les boutons doivent s'afficher et comment la variable `battements`{:class="block3variables"} doit changer. Il est beaucoup plus facile de déboguer un projet si tu sais clairement ce qu'il est censé faire.

--- collapse ---
---
title: Mon tambour ne s'affiche/se masque pas correctement
---

À moins qu'il ne s'agisse du premier tambour, ton tambour doit avoir un script `quand le drapeau est cliqué`{:class="block3events"} pour `cacher`{:class="block3looks"}.

Il devrait y avoir un script `quand je reçois`{:class="block3events"} `ce tambour` pour `montrer`{:class="block3looks"}.

Vérifie que le bouton **Avoir** de ce tambour `envoyer à tous`{:class="block3events"} le même message.

--- /collapse ---

--- collapse ---
---
title: Mon bouton « avoir » ne s’affiche/se masque pas correctement
---

À moins que le bouton ne soit destiné au tout premier tambour, il doit être `caché`{:class="block3looks"} `quand le drapeau est cliqué`{:class="block3events"}.

Il devrait `montrer`{:class="block3looks"} `quand je reçois`{:class="block3events"} le message pour le **tambour précédent**.

Le bouton **avoir** devrait `montrer`{:class="block3looks"} pour informer le joueur du prochain tambour qu'il peut débloquer.

--- /collapse ---

--- collapse ---
---
title: Je peux débloquer un tambour même si je n'ai pas assez de rythmes
---

Vérifie que tu as modifié le nombre de `battements`{:class="block3variables"} nécessaires `quand ce sprite est cliqué`{:class="block3events"} dans le script pour le bouton **avoir** le tambour.

--- /collapse ---

--- collapse ---
---
title: Le nombre de battements ne change pas correctement lorsque je déverrouille un nouveau tambour
---

Vérifie que tu as `ajouter à battements`{:class="block3variables"} un nombre négatif `quand ce sprite est cliqué`{:class="block3events"} dans le script pour le bouton **avoir** le tambour.

Assure-toi que cela correspond au numéro sur le costume de bouton de tambour.

--- /collapse ---

--- /task ---

**Astuce :** si tu t'embrouilles vraiment, tu peux supprimer le nouveau tambour et son bouton, puis recommencer. Parfois, il est difficile de repérer un bug.

--- save ---
