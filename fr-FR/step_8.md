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

Dupliquer le précédent sprite **Avoir**.

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

Ajouter un script à la scène pour `basculer l'arrière-plan`{:class="block3looks"} sur le nouveau décor lorsque le `message`{:class="block3events"} pour ce tambour est reçu.

--- /task ---

Tu constateras peut-être que tes tambours doivent être dans une nouvelle position sur un arrière-plan différent.

--- task ---

Ajoute un script commençant par `quand l'arrière-plan bascule sur`{:class="block3events"} à chaque sprite **tambour** avec un bloc `aller à`{:class="block3motion"} pour les faire changer de position.

Tu devras également définir leur position de départ `quand le drapeau est cliqué`{:class="block3events"}.

--- /task ---

--- task ---

**Tidy:** If you have time, then it's a good idea to make sure the sprites in the sprite list are in a sensible order, starting with the drums in their upgrade order and then the buttons in order.

--- /task ---

--- task ---

**Debug:** First make sure you really understand when the drums and buttons should show and how the `beats`{:class="block3variables"} variable should change. It's much easier to debug a project if you are clear on what it is supposed to do.

--- collapse ---
---
title: My drum doesn't show/hide correctly
---

Unless it is the first drum, your drum should have a `when flag clicked`{:class="block3events"} script to `hide`{:class="block3looks"}. And it should have a `when I receive`{:class="block3events"} `this drum` script to `show`{:class="block3looks"}.

Check that the **Get** button for this drum `broadcasts`{:class="block3events"} the same message.


--- /collapse ---

--- collapse ---
---
title: My Get button doesn't show/hide correctly
---

Unless the button is for the very first drum, then it should `hide`{:class="block3looks"} `when flag clicked`{:class="block3events"}. And it should `show`{:class="block3looks"} `when I receieve`{:class="block3events"} the message for the **previous drum**. The **Get** button should `show`{:class="block3looks"} to let the player know about the next upgrade they are working towards.

--- /collapse ---

--- collapse ---
---
title: I can buy a drum when I don't have enough beats
---

Check that you have changed the number of `beats`{:class="block3variables"} needed `when this sprite clicked`{:class="block3events"} in the script for the **Get** button for the drum.

--- /collapse ---

--- collapse ---
---
title: The number of beats doesn't change correctly when I get a new drum
---

Check that you have `changed beats by`{:class="block3variables"} a negative number `when this sprite clicked`{:class="block3events"} in the script for the **Get** button for the drum.

Make sure this matches the number on the drum button costume.

--- /collapse ---

--- /task ---

--- collapse ---
---
title: Completed project
---

You can view the [completed project here](https://scratch.mit.edu/projects/522323676/){:target="_blank"}.

--- /collapse ---

**Tip:** If you get really muddled then it's fine to delete the new drum and its button, and start again. Sometimes it is hard to spot a bug.

--- save ---
