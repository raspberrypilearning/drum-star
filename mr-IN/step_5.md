## More drums!

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
या टप्प्यात, तुम्ही कोणता ड्रम जोडायचा ते निवडाल.
</div>
<div>
![3 ड्रम असण्यासह पार्टी बॅकड्रॉप दाखवणारा Stage.](images/second-upgrade.png){:width="300px"}
</div>
</div>

--- task ---

**Drum-snare** स्प्राईट डुप्लीकेट करा:

![](images/duplicate-snare-drum.png)

--- /task ---

--- task ---

**Drum Costumes** स्प्राईटवर क्लिक करा आणि **Costumes** टॅब निवडा.

**Choose:** which drum to unlock next. आम्ही **Conga** निवडले.


--- /task ---

--- task ---

तुमच्या निवडलेल्या ड्रमच्या 'hit' आणि 'not hit' कॉश्चुमला तुमच्या नवीन **Drum-snare2** स्प्राईटला ड्रॅग करा:

![एका स्प्राईट मधून दुसऱ्यामधे कॉश्चुम ड्रॅग कसे करायचे हे दाखवणारी ऍनिमेटेड इमेज.](images/drag-costumes.gif)

![कॉश्चुम लीस्ट मधील दोन अतिरीक्त कॉश्चुम सह नवीन स्प्राईटचा पेंट एडिटर.](images/drum-3-costumes.png)

--- /task ---

--- task ---

Name the new drum to match the costumes you chose.

![](images/drum-3-named.png)

--- /task ---

--- task ---

**Code** टॅबवर क्लिक करा. योग्य कॉश्चुम वापरण्यासाठी आणि तुमच्या नवीन ड्रमसाठी साऊंड निवडण्यासाठी कोड बदला.

नवीन ड्रमला `5` वर क्लिक करून तुम्ही मिळवलेल्या बीट्सची संख्या बदला:

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

तुमचा नवीन ड्रम Stage वर पोजिशन करा:

![इतर ड्रमच्या उजवीकडे नवीन ड्रम.](images/drum-3-positioned.png)

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

**Text** टूलवर क्लिक करा आणि नवीन ड्रमची किंमत दाखवण्यासाठी संख्या `30` ने बदला.

![निवडलेल्या ड्रम इमेजसह नवीन बटन कॉश्चुम दाखवणारा पेंट एडिटर आणि टेक्स्ट 30 ला अपडेट केला आहे.](images/get-drum-copy.png)

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

**Party** बॅकड्रॉप जोडा.

--- /task ---

--- task ---

प्लेयर नवीन ड्रमला अपग्रेड करतांना बॅकड्रॉप बदलण्यासाठी Stage ला स्क्रिप्ट जोडा:

![](images/stage-icon.png)

```blocks3
when I receive [conga v] // change to your drum name
switch backdrop to (Party v)
```

--- /task ---

--- task ---

**Test:** Click the green flag to start the game.

You should unlock your new drum if you earn enough beats.

What happens if you click the button before you have earned enough beats?

--- /task ---

--- save ---
