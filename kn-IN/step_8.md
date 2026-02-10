## Challenge

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
ನೀವು ಹೆಚ್ಚು ಹೆಚ್ಚು ಅದ್ಭುತ ವೇದಿಕೆಗಳಲ್ಲಿ ನುಡಿಸುವಾಗ ನಿಮ್ಮ ಪ್ರಾಜೆಕ್ಟ್‌ನ್ನು ಇನ್ನಷ್ಟು ಡ್ರಮ್‌ಗಳು ಮತ್ತು ಹಿನ್ನಲೆಗಳೊಂದಿಗೆ ಅಪ್‌ಗ್ರೇಡ್‌ ಮಾಡಿ. 
</div>
<div>
![](images/upgrade-project.png){:width="300px"}
</div>
</div>

### Add more drums

To add another drum to unlock, look back at the earlier steps of the project.

Here are some reminders if you need them.

--- collapse ---

---
title: For the drum
---

--- task ---

ಹಿಂದಿನ **drum** ಸ್ಪ್ರೈಟ್‌ ನಕಲು ಮಾಡಿ ಮತ್ತು ಎರಡು ಉಡುಪುಗಳನ್ನು ಸೇರಿಸಿ.

--- /ಕಾರ್ಯ ---

--- ಕಾರ್ಯ ---

`when this sprite clicked`{:class="block3events"} ಬರಹದಲ್ಲಿ ಉಪಯೋಗಿಸಿದ `costume`{:class="block3looks"} ಮತ್ತು `sound`{:class="block3sound"} ನ್ನು ಬದಲಾಯಿಸಿ.

--- /ಕಾರ್ಯ ---

--- task ---

`when this sprite clicked`{:class="block3events"} ಬರಹದಲ್ಲಿ ಗಳಿಸಿದ `beats`{:class="block3variables"} ಸಂಖ್ಯೆಗಳನ್ನು ಬದಲಾಯಿಸಿ.

--- /task ---

--- task ---

ಡ್ರಮ್‌ನ್ನು `show`{:class="block3looks"} ಮಾಡುವ `message`{:class="block3events"} ನ್ನು **new drum**ನ ಸಂದೇಶವಾಗಿ ಬದಲಾಯಿಸಿ.

--- /task ---

--- /collapse ---

--- collapse ---

---
title: For the 'Get' button
---

--- task ---

ಹಿಂದಿನ **Get** ಸ್ಪ್ರೈಟ್‌ ನಕಲು ಮಾಡಬೇಕು.

--- /task ---

--- task ---

**previous drum** ನಿಂದ ಬಟನ್‌ನ್ನು `message`{:class="block3events"} `broadcast`{:class="block3events"} ಗೆ ಕಾಣುವಂತೆ ಮಾಡುವ `message`{:class="block3events"}ನ್ನು ಬದಲಾಯಿಸಿ.

--- /task ---

--- task ---

ಹೊಸ ಡ್ರಮ್‌ನ ಬೆಲೆಯನ್ನು ಒಳಗೊಂಡು `costume`{:class="block3looks"} ನ್ನು ಬದಲಾಯಿಸಿ.

--- /task ---

--- task ---

Change the number of `beats`{:class="block3variables"} you must have to unlock this drum in the `if`{:class="block3events"} condition. Change the negative number of `beats`{:class="block3variables"} you `change by`{:class="block3variables"} when you unlock this drum. Change the number that `beats`{:class="block3variables"} needs to be subtracted from in the `join`{:class="block3operators"} block. Change the message that is `broadcast`{:class="block3events"} to the name of the **new drum**.

--- /task ---

--- /collapse ---

--- collapse ---

---
title: For the venue
---

--- task ---

ಹೊಸ ಹಿನ್ನೆಲೆಯನ್ನು ಸೇರಿಸುವುದು.

--- /task ---

--- task ---

Add a script to the Stage to `switch backdrop to`{:class="block3looks"} the new backdrop when the `message`{:class="block3events"} for this drum is received.

--- /task ---

ವಿಭಿನ್ನ ಹಿನ್ನೆಲೆಯಲ್ಲಿ ನಿಮ್ಮ ಡ್ರಮ್‌ಗಳು ಹೊಸ ಸ್ಥಾನದಲ್ಲಿ ಇರಬೇಕು ಎಂದು ನಿಮಗೆ ಕಂಡುಬರಬಹುದು.

--- task ---

Add a script starting with `when backdrop changes to`{:class="block3events"} to each **drum** sprite with a `go to`{:class="block3motion"} block to make them change position.

ನೀವು ಅವುಗಳ ಪ್ರಾರಂಭಿಕ ಸ್ಥಾನವನ್ನೂ ಸಹ ಹೊಂದಿಸಬೇಕು `when flag clicked`{:class="block3events"}.

--- /task ---

--- /collapse ---

### Improve feedback to the player

Tell the player exactly **how many more** beats are needed to unlock the next drum.

--- task ---

Add this code to `join`{:class="block3operators"} the number of beats needed with the text you have used to tell the player they need more beats if they do not have enough to unlock the next drum:

```blocks3
when this sprite clicked
if <(beats)>  [9]> then //if 10 or more beats
hide
change [beats v] by [-10] //take away the cost of upgrade
else
+ say (join ((10) - (beats)) [beats needed!]) for [2] seconds
end
```

**Note**: Update the numbers to match those needed to unlock each drum.

--- /task ---

### Tidy your code

--- task ---

**Tidy:** If you have time, then it's a good idea to make sure the sprites in the sprite list are in a sensible order, starting with the drums in their locked order and then the buttons in order.

--- /task ---

--- task ---

### Stuck?

**ಡಿಬಗ್:** ಮೊದಲಿಗೆ ಡ್ರಮ್‌ಗಳು ಮತ್ತು ಬಟನ್‌ಗಳು ಯಾವಾಗ ತೋರಿಸಬೇಕು ಮತ್ತು ಹೇಗೆ `beats`{:class="block3variables"} ವೇರಿಯೇಬಲ್‌ ಬದಲಾಗಬೇಕು ಎಂಬುವುದು ನಿಮಗೆ ನಿಜವಾಗಿ ಅರ್ಥವಾಗಿದೆ ಎಂದು ಖಚಿತಪಡಿಸಿಕೊಳ್ಳಿ. ಪ್ರಾಜೆಕ್ಟ್‌ ಏನು ಮಾಡಬೇಕು ಎನ್ನುವುದು ನಿಮಗೆ ಸ್ಷಷ್ಟವಾಗಿ ತಿಳಿದಿದ್ದರೆ ಅದನ್ನು ಡಿಬಗ್‌ ಮಾಡುವುದು ತುಂಬಾ ಸುಲಭ.

--- collapse ---
---
title: ನನ್ನ ಡ್ರಮ್‌ ಸರಿಯಾಗಿ ತೋರಿಸುವುದಿಲ್ಲ/ಮರೆಯಾಗುವುದಿಲ್ಲ
---

ಅದು ಮೊದಲ ಡ್ರಮ್‌ ಆಗಿಲ್ಲದಿದ್ದರೆ, ನಿಮ್ಮ ಡ್ರಮ್‌ಗೆ `hide`{:class="block3looks"}ಕ್ಕೆ `when flag clicked`{:class="block3events"} ಬರಹ ಇರಲೇ ಬೇಕು.

It should have a `when I receive`{:class="block3events"} `this drum` script to `show`{:class="block3looks"}.

ಈ ಡ್ರಮ್‌ಗೆ **Get** ಬಟನ್‌ ಅದೇ ಸಂದೇಶವನ್ನು `broadcasts`{:class="block3events"} ಮಾಡುತ್ತದೆ ಎಂದು ಪರಿಶೀಲಿಸಿ.

--- /collapse ---

--- collapse ---
---
title: ನನ್ನ Get ಬಟನ್‌ ಸರಿಯಾಗಿ ತೋರಿಸುತ್ತಿಲ್ಲ/ಮರೆಯಾಗುತ್ತಿಲ್ಲ
---

ಬಟನ್‌ ಮೊಟ್ಟ ಮೊದಲನೆಯ ಡ್ರಮ್‌ಗೆ ಆಗಿಲ್ಲದಿದ್ದರೆ, ಅದು `hide`{:class="block3looks"} `when flag clicked`{:class="block3events"} ಹೊಂದಿರಬೇಕು.

It should `show`{:class="block3looks"} `when I receive`{:class="block3events"} the message for the **previous drum**.

The **Get** button should `show`{:class="block3looks"} to let the player know about the next drum they can unlock.

--- /collapse ---

--- collapse ---
---
title: I can unlock a drum when I don't have enough beats
---

ಡ್ರಮ್‌ಗೆ **Get** ಬಟನ್‌ ಬರಹದಲ್ಲಿ `when this sprite clicked`{:class="block3events"} ಅವಶ್ಯವಿರುವ `beats`{:class="block3variables"}ಸಂಖ್ಯೆಯನ್ನು ನೀವು ಬದಲಾಯಿಸಿರುವುದನ್ನು ಪರಿಶೀಲಿಸಿ.

--- /collapse ---

--- collapse ---
---
title: The number of beats doesn't change correctly when I unlock a new drum
---

ಡ್ರಮ್‌ಗೆ **Get** ಬಟನ್‌ಗೆ `when this sprite clicked`{:class="block3events"}ಬರಹದಲ್ಲಿ ನೀವು`changed beats by`{:class="block3variables"}ನ್ನು ಋಣಾತ್ಮಕ ಸಂಖ್ಯೆಗೆ ಬದಲಾಯಿಸಿದ್ದನ್ನು ಪರಿಶೀಲಿಸಿ.

ಇದು ಡ್ರಮ್‌ ಬಟನ್‌ ಉಡುಪಿನ ಮೇಲಿನ ಸಂಖ್ಯೆಗೆ ಹೊಂದುತ್ತದೆ ಎಂದು ಖಚಿತಪಡಿಸಿಕೊಳ್ಳಿ.

--- /collapse ---

--- /task ---

**ಸಲಹೆ:** ನೀವು ನಿಜವಾಗಿಯೂ ಗೊಂದಲಕ್ಕೊಳಗಾಗಿದ್ದರೆ, ಹೊಸ ಡ್ರಮ್‌ ಮತ್ತು ಅದರ ಬಟನ್‌ ಅಳಿಸಿ ಮತ್ತೆ ಪ್ರಾರಂಭಿಸುವುದು ಉತ್ತಮ. ಕೆಲವೊಮ್ಮೆ ಬಗ್‌ನ್ನು ಪತ್ತೆ ಮಾಡುವುದು ಕಷ್ಟ.

--- save ---
