## Challenge

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
तुम्ही अधिक आश्चर्यकारक ठिकाणी खेळलात त्यामुळे अधिक ड्रम आणि अधिक बॅकड्रॉपसह तुमचा प्रोजेक्ट अपग्रेड करा. 
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

तुमचा आधीचा **drum** स्प्राईट डुप्लीकेट करा आणि दोन कॉश्चुम जोडा.

--- /task ---

--- task ---

`when this sprite clicked`{:class="block3events"} स्क्रिप्टवर क्लिक केले तेव्हा `costume`{:class="block3looks"} आणि `sound`{:class="block3sound"} बदला.

--- /task ---

--- task ---

`when this sprite clicked`{:class="block3events"} स्क्रिप्टमध्ये मिळवलेल्या `beats`{:class="block3variables"} ची संख्या बदला.

--- /task ---

--- task ---

`message`{:class="block3events"} बदला जो ड्रमला **new drum** साठी मेसेज `show`{:class="block3looks"}.

--- /task ---

--- /collapse ---

--- collapse ---

---
title: For the 'Get' button
---

--- task ---

आधीचा **Get** स्प्राईट डुप्लीकेट करा.

--- /task ---

--- task ---

`message`{:class="block3events"} बदला जो बटनला **previous drum** ने `message`{:class="block3events"} `broadcast`{:class="block3events"} दाखवतो.

--- /task ---

--- task ---

नवीन ड्रमच्या किंमतीसह `costume`{:class="block3looks"} बदला.

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

नवीन बॅकड्रॉप जोडणे.

--- /task ---

--- task ---

Add a script to the Stage to `switch backdrop to`{:class="block3looks"} the new backdrop when the `message`{:class="block3events"} for this drum is received.

--- /task ---

तुमचे ड्रम वेगवेगळ्या बॅकड्रॉपवर नवीन पोजिशन मध्ये असण्याची आवश्यकता तुम्हाला कदाचीत जाणवेल.

--- task ---

Add a script starting with `when backdrop changes to`{:class="block3events"} to each **drum** sprite with a `go to`{:class="block3motion"} block to make them change position.

तुम्ही त्यांची सुरूवातीची पोजिशन सुद्धा सेट कराल `when flag clicked`{:class="block3events"}.

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

**डीबग:** ड्रम्स आणि बटन्सने दाखवायला हवे आणि `beats`{:class="block3variables"} व्हेरिएबल बदलायला हवा हे खरोखर तुम्हाला समजले असल्याची खात्री करा. काय करायला हवे हे तुम्हाला स्पष्ट असल्यास प्रोजेक्ट डीबग करणे फार सोपे आहे.

--- collapse ---
---
title: माझा ड्रम योग्यपणे दाखवत नाही/लपवत नाही
---

तो पहिला ड्रम असल्याशिवाय, तुमच्या ड्रमला `hide`{:class="block3looks"} करण्यासाठी `when flag clicked`{:class="block3events"} स्क्रिप्ट असायला हवी.

It should have a `when I receive`{:class="block3events"} `this drum` script to `show`{:class="block3looks"}.

या ड्रमसाठी **Get** बटन सारखाच मेसेज `broadcasts`{:class="block3events"} करतो का ते तपासा.

--- /collapse ---

--- collapse ---
---
title: माझे Get बटन योग्यपणे दाखवत नाही/लपवत नाही
---

बटन फार पहिल्या ड्रमसाठी असल्याशिवाय, ते `hide`{:class="block3looks"} `when flag clicked`{:class="block3events"}.

It should `show`{:class="block3looks"} `when I receive`{:class="block3events"} the message for the **previous drum**.

The **Get** button should `show`{:class="block3looks"} to let the player know about the next drum they can unlock.

--- /collapse ---

--- collapse ---
---
title: I can unlock a drum when I don't have enough beats
---

ड्रमसाठी **Get** बटन साठी स्क्रिप्ट मधील `when this sprite clicked`{:class="block3events"} आवश्यकता असल्यास `beats`{:class="block3variables"} ची संख्या तुम्ही बदललीत का ते तपासा.

--- /collapse ---

--- collapse ---
---
title: The number of beats doesn't change correctly when I unlock a new drum
---

तुम्ही ड्रमसाठी **Get** बटनसाठी स्क्रिप्ट मधील `when this sprite clicked`{:class="block3events"}ऋण संख्या `changed beats by`{:class="block3variables"} केलीत का ते तपासा.

यामुळे ड्रम बटन कॉश्चुमवरील संख्या जुळते याची खात्री करा.

--- /collapse ---

--- /task ---

**टीप:** जर तुम्ही खरोखर गोंधळले असाल तर नवीन ड्रम आणि त्याचे बटण डिलीट करणे आणि पुन्हा सुरू करणे योग्य आहे. काहीवेळा त्रुटी शोधणे कठीण असते.

--- save ---
