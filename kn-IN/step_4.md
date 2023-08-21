## ಮೊದಲನೆಯ ಅಪ್‌ಗ್ರೇಡ್

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
ನೀವು ನಿಮ್ಮ ಮೊದಲನೆಯ ಅಪ್‌ಗ್ರೇಡ್‌ ಸೇರಿಸುತ್ತೀರಿ. ಪ್ರಾರಂಭದಲ್ಲಿ **Get snare** ಬಟನ್‌ ತೋರಿಸುತ್ತದೆ, ಅದರಿಂದ ಆಟಗಾರನಿಗೆ ಅವರು ಯಾವ ಡ್ರಮ್‌ನೆಡೆಗೆ ಕೆಲಸಮಾಡುತ್ತಾರೆ ಎಂದು ತಿಳಿಯುತ್ತದೆ.
</div>
<div>
![](images/first-upgrade.png){:width="300px"}
</div>
</div>

--- task ---

**Drum-snare** ಸ್ಪ್ರೈಟ್‌ನ್ನು ನಿಮ್ಮ ಪ್ರಾಜೆಕ್ಟ್‌ಗೆ ಸೇರಿಸಿ ಮತ್ತು ಅದನ್ನು Stage ಮೇಲೆ ಇರಿಸಿ:

![](images/snare-stage.png)

--- /task ---

--- task ---

**Drum-cymbal** ಸ್ಪ್ರೈಟ್‌ನಿಂದ `when this sprite clicked`{:class="block3events"} ಬರಹವನ್ನು **Drum-snare** ಸ್ಪ್ರೈಟ್‌ಗೆ ಎಳೆಯಿರಿ.

[[[scratch3-copy-code]]]

--- /task ---

--- task ---

ಉಡುಪುಗಳನ್ನು ಮತ್ತು ಡ್ರಮ್‌ ಧ್ವನಿಯನ್ನು ಬದಲಾಯಿಸಿ.

ಗಳಿಸಿದ ಬೀಟ್‌ಗಳ ಸಂಖ್ಯೆಯನ್ನು `2` ಕ್ಕೆ ಬದಲಾಯಿಸಿ:

![](images/snare-icon.png)

```blocks3
when this sprite clicked
+change [beats v] by [2] //2 beats per click
+switch costume to [drum-snare-b v] //hit costume
+play drum [(1) Snare Drum v] for [0.25] beats //drum sound
+switch costume to [drum-snare-a v] //not hit costume
```

--- /task ---

--- task ---

**ಪರೀಕ್ಷೆ:** ನಿಮ್ಮ ಪ್ರಾಜೆಕ್ಟ್‌ನ್ನು ಪ್ರಯತ್ನಿಸಿ. ಸ್ನೇರ್‌ ಡ್ರಮ್‌ ಮೇಲೆ ಕ್ಲಿಕ್‌ ಮಾಡಿದಾಗ ನೀವು 2 ಹೊಡೆತ ಗಳಿಸುವುದನ್ನು ಖಚಿತಪಡಿಸಿಕೊಳ್ಳಿ.

--- /task ---

ನೀವು ಪ್ರಾಜೆಕ್ಟ್‌ನ್ನು ಪ್ರಾರಂಭಿಸಿದಾಗ ಅಪ್‌ಗ್ರೇಡ್‌ಗಳು ಲಭ್ಯವಿರುವುದಿಲ್ಲ. ಅವುಗಳನ್ನು ಹೊಡೆತಗಳ ಜೊತೆಗೆ ಗಳಿಸಬೇಕು.

--- task ---

ಪ್ರಾಜೆಕ್ಟ್‌ನ ಪ್ರಾರಂಭದಲ್ಲಿ ಈ **drum** ಸ್ಪ್ರೈಟ್‌ನ್ನು ಮರೆಮಾಚಲು ಬರಹವನ್ನು ಸೇರಿಸಿ:

![](images/snare-icon.png)

```blocks3
when flag clicked
hide
```

--- /task ---

ಮುಂದಿನ ಅಪ್‌ಗ್ರೇಡ್‌ ಯಾವ ಡ್ರಮ್‌ ಮತ್ತು ಅದರ ಬೆಲೆ ಎಷ್ಟು ಹೊಡೆತಗಳು ಎಂದು ಒಂದು ಬಟನ್‌ ತೋರಿಸುತ್ತದೆ.

--- task ---

**Get** ಸ್ಪ್ರೈಟ್‌ನ್ನು **Duplicate** ಮಾಡಿ:

![](images/duplicate-get.png)

ಅದರ ಕಾಣುವಿಕೆಯನ್ನು **Show** ಗೆ ಬದಲಾಯಿಸಿ ಮತ್ತು ಅದರ ಹೆಸರನ್ನು `Get snare` ಗೆ ಬದಲಾಯಿಸಿ. ಅದನ್ನು Stage ನ ಕೆಳ ಬಲ ಮೂಲೆಯಲ್ಲಿ ಇಡಿ:

![](images/get-snare.png)

--- /task ---

--- task ---

**Drum-snare** ಸ್ಪ್ರೈಟ್‌ ಮೇಲೆ ಕ್ಲಿಕ್‌ ಮಾಡಿ ಮತ್ತು **Costumes** ಟ್ಯಾಬ್‌ಗೆ ಹೋಗಿ. ನಿಮ್ಮ ಡ್ರಮ್‌ಗೆ ಹೊಡೆತ ಆಗದೇ ಇರುವ ಉಡುಪನ್ನು ಹೈಲೈಟ್‌ ಮಾಡಲು **Select** (ಬಾಣ) ಟೂಲ್‌ ಉಪಯೋಗಿಸಿ. **Group** iಐಕಾನ್‌ ಮೇಲೆ ಕ್ಲಿಕ್‌ ಮಾಡಿ ಮತ್ತು ನಂತರ **Copy** ಐಕಾನ್:

![](images/snare-icon.png)

![](images/copy-costume.png)

--- /task ---

--- task ---

ನಿಮ್ಮ **Get snare** ಸ್ಪ್ರೈಟ್‌ ಮೇಲೆ ಕ್ಲಿಕ್‌ ಮಾಡಿ ಮತ್ತು ಸ್ನೇರ್‌ ಉಡುಪನ್ನು **Paste** ಮಾಡಿ. ನಿಮ್ಮ ಬಟನ್‌ಗೆ ಸರಿಹೊಂದಲು ಅದರ ಗಾತ್ರ ಬದಲಾವಣೆ ಮತ್ತು ಸ್ಥಾನ ಬದಲಾವಣೆಯನ್ನು ಮಾಡಬೇಕಾಗಬಹುದು:

![](images/get-snare-icon.png)

![](images/paste-costume.png)

--- /task ---

--- task ---

**Code** ಟ್ಯಾಬ್‌ ಮೇಲೆ ಕ್ಲಿಕ್‌ ಮಾಡಿ ಮತ್ತು ಪ್ರಾಜೆಕ್ಟ್‌ ಪ್ರಾರಂಭದಲ್ಲಿ **Get snare** ಸ್ಪ್ರೈಟ್‌ ತೋರಿಸಲು ಬರಹ ಸೇರಿಸಿ:

![](images/get-snare-icon.png)

```blocks3
when flag clicked
show
```

--- /task ---

ಬಳಕೆದಾರ `10` ಅಥವಾ ಹೆಚ್ಚು ಹೊಡೆತಗಳನ್ನು ಹೊಂದಿದ್ದರೆ ಮಾತ್ರ ಅಪ್‌ಗ್ರೇಡ್‌ನ್ನು ಖರೀದಿಸಬಹುದು. [Grow a dragonfly](https://projects.raspberrypi.org/en/projects/grow-a-dragonfly){:target="_blank"}ರಲ್ಲಿ, ನೀವು `if`{:class="block3control"} ಬ್ಲಾಕ್‌ಗಳೊಂದಿಗೆ ತೀರ್ಮಾನ ಮಾಡುವುದರ ಬಗೆಗೆ ಕಲಿತಿದ್ದೀರಿ.

`if ... else`{:class="block3control"} ಬ್ಲಾಕ್‌ನ್ನು ತೀರ್ಮಾನ ಮಾಡಲು ಉಪಯೋಗಿಸಿದರೆ ಮತ್ತು ಷರತ್ತು `true` ಅಥವಾ `false` ಆದರೆ ವಿಭಿನ್ನ ಸಂಗತಿಗಳನ್ನು ಮಾಡುತ್ತದೆ.

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
ನಾವು <span style="color: #0faeb0">**if ... else**</span> ನ್ನು ತೀರ್ಮಾನ ಮಾಡಲು ಯಾವಾಗಲೂ ಉಪಯೋಗಿಸುತ್ತೇವೆ. ನೀವು ನಿದ್ದೆಯಿಂದ ಎದ್ದಾಗ, ನೀವು `if`{:class="block3control"} ಇದು ಮುಂಜಾನೆಯೇ ಎಂದು ಪರಿಶೀಲಿಸುತ್ತೀರಿ. ನೀವು ಎದ್ದೇಳುತ್ತೀರಿ, ಅಥವಾ `else`{:class="block3control"} ನೀವು ಮತ್ತೆ ಮಲಗಲು ಹೋಗುತ್ತೀರಿ. ನೀವು ಮಾಡುವ ಯಾವುದಾದರೂ `if ... else`{:class="block3control"} ತೀರ್ಮಾನಗಳ ಬಗೆಗೆ ಯೋಚಿಸಬಹುದೇ? 
</p>

--- task ---

Add this code to get the upgrade `if`{:class="block3control"} the player has enough beats, or `say`{:class="block3looks"} `More beats needed!` if they are not able to upgrade:

![](images/get-snare-icon.png)

```blocks3
when this sprite clicked
if <(beats)>  [9]> then //if 10 or more beats
hide
change [beats v] by [-10] //take away the cost of upgrade
else
say [More beats needed!] for [2] seconds 
end
```

--- /task ---

Instead of only telling the player they need **more** beats, you can tell the player exactly **how many more** beats are needed to get the upgrade.

A `join`{:class="block3operators"} block is used to concatenate, or 'link' two values together.

![](images/get-snare-icon.png)

--- task ---

Add this code to `join`{:class="block3operators"} the number of beats needed with the text you have used to tell the player they need more beats if they are not able to upgrade:

```blocks3
when this sprite clicked
if <(beats)>  [9]> then //if 10 or more beats
hide
change [beats v] by [-10] //take away the cost of upgrade
else
+ say (join ((10) - (beats)) [beats needed!]) for [2] seconds
end
```

--- /task ---

--- task ---

Add a `broadcast`{:class="block3events"} block to send a new `snare` message:

![](images/get-snare-icon.png)

```blocks3
when this sprite clicked
if <(beats)>  [9]> then // if 10 or more beats
hide
change [beats v] by [-10] // take away the cost of upgrade
+ broadcast [snare v] // your drum name
else
say (join ((10) - (beats)) [beats needed!]) for [2] seconds
end
```

--- /task ---

--- task ---

Click on the **Drum-snare** sprite. Add this script:

![](images/snare-icon.png)

```blocks3
when I receive [snare v]
show
```

--- /task ---

When you upgrade your equipment, you will be able to play at bigger venues.

--- task ---

Add another backdrop. We chose **Chalkboard** to play our second gig at school.

Add code to the Stage to `switch backdrop`{:class="block3looks"} when the upgrade message is received:

![](images/stage-icon.png)

```blocks3
when I receive [snare v]
switch backdrop to [Chalkboard v]
```

**Tip:** Choose a venue that's a small step up from the bedroom. You want to save bigger venues for later.

--- /task ---

--- task ---

**Test:** Run your project. Try and buy the snare upgrade before you have enough beats.

When you buy the upgrade check: the snare appears, the button disappears, the venue changes and the `beats`{:class="block3variables"} go down by `10`.

--- /task ---

--- save ---
