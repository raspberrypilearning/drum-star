## Mise en place de la scène

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Dans cette étape, tu prépareras la scène pour ton premier concert et choisiras un nom de rockstar.
</div>
<div>
![](images/set-the-stage.png){:width="300px"}
</div>
</div>

--- task ---

Ouvre le [projet de démarrage Star du tambour](https://scratch.mit.edu/projects/535783147/editor){:target="_blank"}. Scratch s'ouvrira dans un autre onglet du navigateur.

[[[working-offline]]]

--- /task ---

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
Des musiciens appelés <span style="color: #0faeb0">**artistes bricoleurs**</span> commencent à enregistrer de la musique depuis leur chambre. Ils produisent eux-mêmes leurs propres chansons puis les publient en ligne pour que tout le monde puisse les entendre. 
</p>

Le jeu commence dans une chambre comme un artiste bricoleur.

--- task ---

Clique sur **Choisir un arrière-plan** et recherche `bedroom`.

**Choisir :** Sélectionne une chambre et ajoute-la à ton projet. Nous avons choisi `Bedroom 3`.

![La scène montrant l'arrière-plan "Bedroom 3".](images/bedroom3.png)

--- /task ---

--- task ---

Dans Scratch, tu peux ajouter du code à la scène.

Clique sur l'arrière-plan de ta chambre dans le volet Scène et ajoute ce code :

![L'arrière-plan dans le volet de scène.](images/bedroom-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //ton nom d'arrière-plan
```

--- /task ---

Chaque musicien doit choisir un nom de rockstar.

Une **variable** est un moyen de stocker des nombres et/ou du texte. Ton nom de rockstar sera stocké dans une `variable`{:class="block3variables"} afin qu'il puisse être utilisé à tout moment.

--- task ---

Dans le menu des blocs `Variables`{:class="block3variables"}, clique sur le bouton **Créer une variable**.

Appelle ta nouvelle variable `nom` :

![La fenêtre contextuelle Nouvelle variable avec la saisie de texte "nom".](images/new-variable.png)

**Remarque :** La nouvelle variable `nom` apparaît sur la scène et peut désormais être utilisée dans les blocs `Variable`{:class="block3variables"}.

--- /task ---

--- task ---

Au départ du projet, ton nom de rockstar est inconnu.

Ajoute un bloc à `mettre nom à`{:class="block3variables"} `???` :

![](images/stage-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //ton nom d'arrière-plan
+ set [nom v] to [???] //ta variable
```

--- /task ---

Tu peux `demander`{:class="block3sensing"} une question dans Scratch, puis utiliser une `variable`{:class="block3variables"} pour stocker la `réponse`{:class="block3sensing"}.

--- task ---

Clique sur le menu des blocs `Capteurs`{:class="block3sensing"} et ajoute un bloc `demander`{:class="block3sensing"} à ton code :

![](images/stage-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //ton nom d'arrière-plan
set [nom v] to [???] //ta variable
+ ask [Quel est ton nom de rockstar ?] and wait //ta question
```

--- /task ---

--- task ---

Définis la `variable`{:class="block3variables"} `nom`{:class="block3variables"} avec la `réponse`{:class="block3sensing"} :

![](images/stage-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //ton nom d'arrière-plan
set [nom v] to [???] //ta variable
ask [Quel est ton nom de rockstar ?] and wait //ta question
+ set [nom v] to (answer)
```

--- /task ---

Modifie l'apparence de ta `variable`{:class="block3variables"} sur la scène.

--- task ---

Fais un clic droit sur la `variable`{:class="block3variables"} sur la scène et choisis **grande lecture** :

![](images/large-readout.png)

--- /task ---

--- task ---

Fais glisser ta `variable`{:class="block3variables"} pour la positionner en haut à droite de la scène :

![](images/repositioned-variable.png)

--- /task ---

--- task ---

**Test :** Exécute ton projet pour t'assurer que la `variable`{:class="block3variables"} commence par `???` puis met à jour ta `réponse`{:class="block3sensing"}.

--- /task ---

--- task ---

Maintenant que tu as testé que la `variable`{:class="block3variables"} devient la `réponse`{:class="block3sensing"}, tu peux faire glisser les 2 derniers blocs de code loin du reste du script. Cela signifie que tu n'as pas besoin de saisir une `réponse`{:class="block3sensing"} à chaque fois que tu testes ton projet :

![](images/stage-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //ton nom d'arrière-plan
set [nom v] to [???] //ta variable
```

```blocks3
ask [Quel est ton nom de rockstar ?] and wait //ta question
set [nom v] to (answer)
```

--- /task ---

--- save ---
