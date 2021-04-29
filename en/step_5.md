## Second upgrade

Your drum skills are improving, time for a second upgrade.

--- task ---

Add the **Snare** drum sprite to your project and position it on the Stage.

--- /task ---

--- task ---

Drag the `when this sprite clicked`{:class="block3events"} script from the **Highhat** to the **Snare** sprite.

Change the code to use the correct costumes and choose a sound for your new drum.

Change the number of beats you earn by clicking the new drum to `5`.

--- /task ---

Next, you need a button so that players can upgrade to this new drum.

--- task ---

Duplicate the **Get highhat** sprite.

Position it in the bottom-right corner of the Stage and change its name to 'Get snare':

![desc](images/get-snare.png)

--- /task ---

--- task ---

Delete the Highhat from the costume and copy and paste the Snare drum to the costume. 

Change the number to `30` to show the cost of the snare drum.

Your button should look like this:

![desc](images/get-sname-costume.png)

--- /task ---

--- task ---

Drag the three scripts from the first Get sprite to your new Get sprite.

--- /task ---

--- task ---

Change the event that makes the button show:

```blocks3
+when I receive [highhat v]
show
```

This will make the button appear when the Hihat appears on Stage and the Snare is the next one available. 

--- /task ---


