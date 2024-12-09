## More drums!

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
ಈ ಹಂತದಲ್ಲಿ, ನೀವು ಯಾವ ಡ್ರಮ್‌ ಸೇರಿಸಬೇಕೆಂದು ಆಯ್ಕೆ ಮಾಡುತ್ತೀರಿ.
</div>
<div>
![3 ಡ್ರಮ್‌ಗಳಿರುವ ಪಾರ್ಟಿ ಹಿನ್ನೆಲೆ ತೋರಿಸುತ್ತಿರುವ Stage.](images/second-upgrade.png){:width="300px"}
</div>
</div>

--- task ---

**Drum-snare** ಸ್ಪ್ರೈಟ್‌ ನಕಲು ಮಾಡಿ:

![](images/duplicate-snare-drum.png)

--- /task ---

--- task ---

**Drum Costumes** ಸ್ಪ್ರೈಟ್‌ ಕ್ಲಿಕ್‌ ಮಾಡಿ ಮತ್ತು **Costumes** ಟ್ಯಾಬ್‌ ಆಯ್ಕೆ ಮಾಡಿ.

**Choose:** which drum to unlock next. ನಾವು **Conga** ಆಯ್ದುಕೊಂಡಿದ್ದೇವೆ.


--- /task ---

--- task ---

ನಿಮ್ಮ ಆಯ್ಕೆಯ ಡ್ರಮ್‌ನ 'hit' ಮತ್ತು 'not hit'ಉಡುಪುಗಳನ್ನು ನಿಮ್ಮ ಹೊಸ **Drum-snare2** ಸ್ಪ್ರೈಟ್‌ಗೆ ಎಳೆಯಿರಿ:

![ಒಂದು ಸ್ಪ್ರೈಟ್‌ನಿಂದ ಇನ್ನೊಂದಕ್ಕೆ ಉಡುಪುಗಳನ್ನು ಹೇಗೆ ಎಳೆಯುವುದು ಎಂದು ತೋರಿಸುವ ಅನಿಮೇಟೆಡ್‌ ಚಿತ್ರ.](images/drag-costumes.gif)

![ಉಡುಪುಗಳ ಲಿಸ್ಟ್‌ನಲ್ಲಿ ಎರಡು ಅಧಿಕ ಉಡುಪುಗಳೊಂದಿಗೆ ಹೊಸ ಸ್ಪ್ರೈಟ್‌ನ ಪೇಂಟ್‌ ಎಡಿಟರ್.](images/drum-3-costumes.png)

--- /task ---

--- task ---

Name the new drum to match the costumes you chose.

![](images/drum-3-named.png)

--- /task ---

--- task ---

**Code** ಟ್ಯಾಬ್ ಮೇಲೆ ಕ್ಲಿಕ್ ಮಾಡಿ. ಸರಿಯಾದ ಉಡುಪುಗಳನ್ನು ಉಪಯೋಗಿಸಲು ಕೋಡ್‌ ಬದಲಾಯಿಸಿ ಮತ್ತು ನಿಮ್ಮ ಹೊಸ ಡ್ರಮ್‌ಗೆ ಶಬ್ದವನ್ನು ಆಯ್ಕೆ ಮಾಡಿಕೊಳ್ಳಿ.

ಹೊಸ ಡ್ರಮ್‌ನ್ನು `5`ಗೆ ಕ್ಲಿಕ್‌ ಮಾಡಿ ನೀವು ಗಳಿಸುವ ಹೊಡೆತಗಳ ಸಂಖ್ಯೆಯನ್ನು ಬಸಲಾಯಿಸಿ:

![](images/drum-3-icon.png)

```blocks3
when this sprite clicked
+change [beats v] by [5] //5 beats per click
+switch costume to [ v] //your hit costume
+play drum [ v] for [0.25] beats //your drum sound
+switch costume to [ v] //your not hit costume
```

--- /task ---

--- task ---

ನಿಮ್ಮ ಹೊಸ ಡ್ರಮ್‌ನ್ನು Stage ಮೇಲೆ ಸ್ಥಾನಕ್ಕೆ ಎಳೆಯಿರಿ:

![ಉಳಿದ ಡ್ರಮ್‌ಗಳ ಬಲಭಾಗಕ್ಕೆ ಹೊಸ ಡ್ರಮ್‌.](images/drum-3-positioned.png)

--- /task ---

Add a button so that players can unlock the new drum.

--- task ---

Duplicate the **Get snare** sprite and position it in the bottom-right corner of the Stage.

--- /task ---

--- task ---

Change its name (for example `Get conga`):

![The Sprite list with duplicated 'Get snare' sprite. The sprite name has been changed to match the new drum type and positioned in the bottom-right of the Stage.](images/get-drum-3.png)

--- /task ---

--- task ---

Delete the **snare drum** from the new 'Get' button costume.

--- /task ---

--- task ---

Copy the 'not hit' costume for your new drum and paste it to the new 'Get' button costume.

--- /task ---

--- task ---

**Text** ಟೂಲ್‌ ಮೇಲೆ ಕ್ಲಿಕ್‌ ಮಾಡಿ ಮತ್ತು ಹೊಸ ಡ್ರಮ್‌ನ ಬೆಲೆಯನ್ನು ತೋರಿಸಲು ಸಂಖ್ಯೆಯನ್ನು`30` ಕ್ಕೆ ಬದಲಾಯಿಸಿ.

![ಆಯ್ಕೆ ಮಾಡಿದ ಡ್ರಮ್‌ ಚಿತ್ರ ಮತ್ತು ಪಠ್ಯವನ್ನು 30ಕ್ಕೆ ನವೀಕರಿಸುವುದರೊಂದಿಗೆ ಹೊಸ ಬಟನ್‌ ಉಡುಪು ತೋರಿಸುವ ಪೇಂಟ್‌ ಎಡಿಟರ್.](images/get-drum-copy.png)

--- /task ---

Your new 'Get' button should `hide`{:class="block3looks"} at the start.

--- task ---

![](images/get-drum-3-icon.png)

```blocks3
when flag clicked
+ hide
```

--- /task ---

--- task ---

Add a `when I receive`{:class="block3events"} script that your new 'Get' button will `show`{:class="block3looks"} when the player unlocks the snare drum.

```blocks3
when I receive [snare v] // appear when previous drum is unlocked
show // show button to get the new drum
```

--- /task ---

--- task ---

Change:
- The number of beats needed to unlock this drum
- The number of beats that are removed when the player unlocks this drum.
- The message that is `broadcast`{:class="block3events"} when the player gets the new drum.

```blocks3
when this sprite clicked
if <(beats)>  [29]> then // change to 29
hide
change [beats v] by [-30] // change to -30
broadcast (conga v) // change to your drum name
else
say [More beats needed!] for [2] seconds 
end
```

--- /task ---

--- task ---

Click your new drum sprite and change the `when I receive snare`{:class="block3events"} script to show it when your new drum is unlocked:

```blocks3
when I receive [conga v] // change to your drum name
show
```

--- /task ---

--- task ---

**Party** ಹಿನ್ನೆಲೆಯನ್ನು ಸೇರಿಸಿ.

--- /task ---

--- task ---

ಆಟಗಾರ ಹೊಸ ಡ್ರಮ್‌ಗೆ ಅಪ್‌ಗ್ರೇಡ್‌ ಆದಾಗ ಹಿನ್ನೆಲೆ ಬದಲಾಯಿಸಲು Stage ಗೆ ಬರಹ ಸೇರಿಸಿ:

![](images/stage-icon.png)

```blocks3
when I receive [conga v] // change to your drum name
switch backdrop to (Party v)
```

--- /task ---

--- task ---

**Test:** Click the green flag to start the game.

You should get unlock your new drum if you earn enough beats.

What happens if you click the button before you have earned enough beats?

--- /task ---

--- save ---
