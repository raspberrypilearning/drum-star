## Second upgrade

Your drum skills are improving, time for a second upgrade. This time you will choose a drum.

--- task ---

Duplicate the **Drum-snare** sprite:

![desc](images/duplicate-snare-drum.png)

--- /task ---

The Drum costumes sprite has lots of drum costumes for you to choose from.

--- task ---

Click on the **Drum costumes** sprite and select the **Costumes** tab.

**Choose:** a drum for the next upgrade. We chose **Drums Conga**.

Drag the 'hit' and 'not hit' costumes of your chosen drum to your new **Drum-snare2** sprite:

![desc](images/drag-costumes.gif)

![desc](images/drum-3-costumes.png)


--- /task ---

--- task ---

Name your drum to match the costumes you chose.

![desc](images/drum-3-named.png)

--- /task ---

--- task ---

Click on the **Code** tab. Change the code to use the correct costumes and choose a sound for your new drum.

Change the number of beats you earn by clicking the new drum to `5`:

![desc](images/drum-3-icon.png)

```blocks3
when this sprite clicked
+change [beats v] by [5] //5 beats per click
+switch costume to [ v] //your hit costume
+play drum [ v] for [0.25] beats //your drum sound
+switch costume to [ v] //your not hit costume
```

--- /task ---

--- task ---

Drag your new drum into position on the Stage:

![desc](images/drum-3-positioned.png)

--- /task ---

Next, you need a button so that players can upgrade to this new drum.

--- task ---

Duplicate the **Get** sprite.

Position it in the bottom-right corner of the Stage and change its name to 'Get' and then the name of your new drum:

![desc](images/get-drum-3.png)

--- /task ---

--- task ---

Copy and paste the 'not hit' costume for your new drum to the button costume. 

![desc](images/get-drum-copy.png)

--- /task ---

--- task ---

Click on the **Text** tool and change the number to `30` to show the cost of the new drum.

Your button should look like this:

![desc](images/get-drum-30.png)

--- /task ---

This button should hide at the start then appear when the player upgrades to the snare drum so they know which drum they are working towards.

--- task ---

Add a `when I recieve`{:class="block3events"} script that your new drum button will show as the next upgrade when the player gets the **Drum-snare** drum:

![desc](images/get-drum-3-icon.png)

```blocks3
when I receive [snare v]
show
```

--- /task ---

--- task ---

Change the `when flag clicked`{:class="block3events"} script to `hide`{:class="block3looks"} instead of `hide`{:class="block3looks"}:

![desc](images/get-drum-3-icon.png)

```blocks3
when flag clicked
-show
+hide
```

--- /task ---

--- task ---

Change the number of beats needed to buy this drum and the number of beats that are removed when the player gets this drum. 

Also change the message that is `broadcast`{:class="block3events"} when the player gets the new drum to match the new drum: 



```blocks3
when this sprite clicked
+if <(beats)>  [29]> then // change to 29
hide
+change [beats v] by [-30] // change to 30
+ broadcast [conga v] // change to your drum name
else
say [Not enough beats!] for [2] seconds 
end
```
--- /task ---

--- task ---

Add the Party backdrop.

Add a script to the Stage to switch backdrop when the player upgrades to the new drum:

![desc](images/stage-icon.png)

```blocks3
when I receive [conga v] // change to your drum name
switch backdrop to (Party v)
```

--- /task ---

--- task ---

**Test:** Click the green flag to start the game and test that you can earn enough beats to get your new drum. 

What happens if you click the button before you have earned enough beats?

--- /task ---

