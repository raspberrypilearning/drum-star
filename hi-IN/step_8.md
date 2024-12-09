## Challenge

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
जैसे जैसे आप और अधिक अद्भुत जगहों पर बजाते हैं अपने प्रोजेक्ट को और अधिक ड्रम और अधिक बैकड्रॉप के साथ अपग्रेड करें। 
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

पहले के **drum** स्प्राइट को डुप्लिकेट करें और दो पोशाक जोड़ें।

--- /task ---

--- task ---

`when this sprite clicked`{:class="block3events"} स्क्रिप्ट में उपयोग किए गये `costume`{:class="block3looks"} और `sound`{:class="block3sound"} को बदलें।

--- /task ---

--- task ---

`when this sprite clicked`{:class="block3events"} स्क्रिप्ट में अर्जित किए गये `beats`{:class="block3variables"} की संख्या बदलें।

--- /task ---

--- task ---

`message`{:class="block3events"} जो ड्रम को `show`{:class="block3looks"} दिखाता है को **new drum** संदेश में बदलें।

--- /task ---

--- /collapse ---

--- collapse ---

---
title: For the 'Get' button
---

--- task ---

पहले के **Get** स्प्राइट को डुप्लिकेट करें।

--- /task ---

--- task ---

`message`{:class="block3events"} बटन जो `message`{:class="block3events"} `broadcast`{:class="block3events"} में दिखता है उसको **previous drum** से बदलें

--- /task ---

--- task ---

`costume`{:class="block3looks"} और नये ड्रम के मूल्य को बदलें।

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

एक और पृष्ठभूमि जोड़ें।

--- /task ---

--- task ---

Add a script to the Stage to `switch backdrop to`{:class="block3looks"} the new backdrop when the `message`{:class="block3events"} for this drum is received.

--- /task ---

ऐसा हो सकता है की आपको लगे कि आपके ड्रम को एक अलग पृष्ठभूमि पर एक नई स्थिति में होना चाहिए।

--- task ---

Add a script starting with `when backdrop changes to`{:class="block3events"} to each **drum** sprite with a `go to`{:class="block3motion"} block to make them change position.

आपको प्रारंभिक स्थिति को `when flag clicked`{:class="block3events"} पर भी सेट करना होगा।

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

**डीबग:** पहले सुनिश्चित करें कि आप वास्तव में समझते हैं कि ड्रम और बटन कब दिखाना चाहिए और `beats`{:class="block3variables"} वेरिएबल कैसे बदलना चाहिए। किसी प्रोजेक्ट को डिबग करना बहुत आसान है यदि आप इस बारे में स्पष्ट हैं कि उसे क्या करना है।

--- collapse ---
---
title: मेरा ड्रम ठीक से दिखाई नहीं देता /छुपाता नहीं है
---

जब तक कि यह पहला ड्रम न हो, आपके ड्रम में `when flag clicked`{:class="block3events"} स्क्रिप्ट होना चाहिए ताकि `hide`{:class="block3looks"}।

It should have a `when I receive`{:class="block3events"} `this drum` script to `show`{:class="block3looks"}.

जांचें कि इस ड्रम के लिए <**Get** बटन एक ही संदेश `broadcasts`{:class="block3events"} करे।

--- /collapse ---

--- collapse ---
---
title: मेरा Get बटन सही ढंग से दिखाई नहीं देता /छुपाता नहीं है
---

जब तक बटन पहले ड्रम के लिए न हो, तब इसे `hide`{:class="block3looks"} `when flag clicked`{:class="block3events"}।

It should `show`{:class="block3looks"} `when I receive`{:class="block3events"} the message for the **previous drum**.

The **Get** button should `show`{:class="block3looks"} to let the player know about the next drum they can unlock.

--- /collapse ---

--- collapse ---
---
title: I can unlock a drum when I don't have enough beats
---

जब ड्रम के लिए **Get**बटन स्क्रिप्ट `when this sprite clicked`{:class="block3events"} तो जाँचें की आपने जितनी ज़रूरत हो उतनी `beats`{:class="block3variables"} बदली हैं ।

--- /collapse ---

--- collapse ---
---
title: The number of beats doesn't change correctly when I unlock a new drum
---

जब ड्रम के लिए **Get**बटन स्क्रिप्ट `when this sprite clicked`{:class="block3events"} तो जाँचें कीआपने `changed beats by`{:class="block3variables"}को एक ऋणात्मक संख्या में बदला है।

सुनिश्चित करें कि यह ड्रम बटन पोशाक पर संख्या से मेल खाता है।

--- /collapse ---

--- /task ---

**सुझाव:** यदि आप वास्तव में अव्यवस्थित हो जाते हैं तो नया ड्रम और उसके बटन को हटाना ठीक है, और फिर से शुरू करें। कभी-कभी बग का पता लगाना मुश्किल होता है।

--- save ---
