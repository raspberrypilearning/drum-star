## First upgrade

Now you can add your first upgrade. 

--- task ---

Duplicate the **Drum costumes** sprite again and choose a second drum. We chose Highhat.

Name the new sprite to match and set it to `show`. 

Position the sprite on the Stage.

![](images/highhat-sprite.png)

--- /task ---

--- task ---

Drag the `when this sprite clicked`{:class="block3events"} script from your first drum to your new drum.

[[[]]]

--- /task ---

--- task ---

Change the costumes and the drum sound.

Change the number of beats earned to `2`.

![](images/highhat-icon.png)

```blocks3
when this sprite clicked
+change [beats v] by [2]
+switch costume to [drum-highhat-b v] //your hit costume
+play drum ((6) Closed High-Hat v) for [0.25] beats //your drum sound
+switch costume to [drum-highhat-a v] //your unhit costume
```

--- /task ---

--- task ---

**Test:** Try out your project. Make sure to test your new drum.  

--- /task ---

Upgrades are not available when you start the project, they have to be earned with beats. 

--- task ---

Add a script to hide this drum sprite at the start of the project:

![](images/highhat-icon.png)

```blocks3
when flag clicked
hide
```

--- /task ---

--- task ---

Drag the 

--- /task ---

--- task ---

Duplicate the 'get' sprite and

--- /task ---