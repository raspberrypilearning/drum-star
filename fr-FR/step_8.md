## Améliorer ton projet

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Améliore ton projet avec plus de tambours et plus de décors à mesure que tu joues dans des salles plus prestigieuses. 
</div>
<div>
![](images/upgrade-project.png){:width="300px"}
</div>
</div>

Il y a beaucoup plus de costumes de tambour parmi lesquels choisir pour ajouter plus d'améliorations à ton projet.

Pour ajouter un autre tambour à améliorer, reviens aux étapes précédentes du projet.

Pour le **tambour**, il te faudra :

--- task ---

Dupliquer le précédent sprite **tambour** et ajouter deux costumes.

--- /task ---

--- task ---

Modifier le `costume`{:class="block3looks"} et le `son`{:class="block3sound"} utilisés dans le script `Quand ce sprite est cliqué`{:class="block3events"}.

--- /task ---

--- task ---

Modifier le nombre de `battements`{:class="block3variables"} gagnés dans le script `quand ce sprite est cliqué`{:class="block3events"}.

--- /task ---

--- task ---

Changer le `message`{:class="block3events"} qui fait que le tambour `montre`{:class="block3looks"} un message pour le **nouveau tambour**.

--- /task ---

Pour le **bouton**, il te faudra :

--- task ---

Dupliquer le précédent sprite **avoir**.

--- /task ---

--- task ---

Changer le `message`{:class="block3events"} qui fait apparaître le bouton au `message`{:class="block3events"} `diffusé`{:class="block3events"} par le **tambour précédent**.

--- /task ---

--- task ---

Changer le `costume`{:class="block3looks"} ainsi que le coût du nouveau tambour.

--- /task ---

--- task ---

Modifier le nombre de `battements`{:class="block3variables"} que tu dois avoir pour obtenir ce tambour dans la condition `si`{:class="block3events"}. Changer le nombre négatif de `battements`{:class="block3variables"} que tu `mets`{:class="block3variables"} lorsque tu obtiens ce tambour. Remplacer le message qui obtient `envoyé à tous`{:class="block3events"} par le nom du **nouveau tambour**.

--- /task ---

Pour la **salle**, il te faudra :

--- task ---

Ajouter un nouvel arrière-plan.

--- /task ---

--- task ---

Ajouter un script à la scène pour `basculer sur l'arrière-plan`{:class="block3looks"} sur le nouveau décor lorsque le `message`{:class="block3events"} pour ce tambour est reçu.

--- /task ---

Tu constateras peut-être que tes tambours doivent être dans une nouvelle position sur un arrière-plan différent.

--- task ---

Ajoute un script commençant par `quand l'arrière-plan bascule sur`{:class="block3events"} à chaque sprite **tambour** avec un bloc `aller à`{:class="block3motion"} pour les faire changer de position.

Tu devras également définir leur position de départ `quand le drapeau est cliqué`{:class="block3events"}.

--- /task ---

--- task ---

**Bien rangé :** Si tu as le temps, alors c'est une bonne idée de t'assurer que les sprites dans la liste des sprites sont dans un ordre raisonnable, en commençant par les tambours dans leur ordre d'amélioration, puis les boutons dans l'ordre.

--- /task ---

--- task ---

**Débogage :** Assure-toi d'abord que tu comprends vraiment quand le tambour et les boutons doivent s'afficher et comment la variable `battements`{:class="block3variables"} doit changer. Il est beaucoup plus facile de déboguer un projet si tu sais clairement ce qu'il est censé faire.

--- collapse ---
---
title: Mon tambour ne s'affiche/se cache pas correctement
---

À moins qu'il ne s'agisse du premier tambour, ton tambour doit avoir un script `quand le drapeau est cliqué`{:class="block3events"} pour `cacher`{:class="block3looks"}. Et il devrait avoir un script `quand je reçois`{:class="block3events"} `ce tambour` pour `montrer`{:class="block3looks"}.

Vérifie que le bouton **Avoir** de ce tambour `envoyer à tous`{:class="block3events"} le même message.


--- /collapse ---

--- collapse ---
---
title: Mon bouton Avoir ne s'affiche/ne se cache pas correctement
---

À moins que le bouton ne soit destiné au tout premier tambour, il doit être `caché`{:class="block3looks"} `quand le drapeau est cliqué`{:class="block3events"}. Et il devrait se `montrer`{:class="block3looks"} `quand je reçois`{:class="block3events"} le message pour le **tambour précédent**. Le bouton **Avoir** doit s'`afficher`{:class="block3looks"} pour informer le joueur de la prochaine amélioration vers laquelle il travaille.

--- /collapse ---

--- collapse ---
---
title: Je peux acheter un tambour quand je n'ai pas assez de battements
---

Vérifie que tu as modifié le nombre de `battements`{:class="block3variables"} nécessaires `quand ce sprite est cliqué`{:class="block3events"} dans le script pour le bouton **avoir** le tambour.

--- /collapse ---

--- collapse ---
---
title: Le nombre de battements ne change pas correctement lorsque je reçois un nouveau tambour
---

Vérifie que tu as `ajouter à battements`{:class="block3variables"} un nombre négatif `quand ce sprite est cliqué`{:class="block3events"} dans le script pour le bouton **avoir** le tambour.

Assure-toi que cela correspond au numéro sur le costume de bouton de tambour.

--- /collapse ---

--- /task ---

--- collapse ---
---
title: Le projet terminé
---

Tu peux voir le [projet terminé ici](https://scratch.mit.edu/projects/707230907/){:target="_blank"}.

--- /collapse ---

**Astuce :** Si tu t'embrouilles vraiment, tu peux supprimer le nouveau tambour et son bouton, puis recommencer. Parfois, il est difficile de repérer un bug.

--- save ---
