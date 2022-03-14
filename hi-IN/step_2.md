## मंच तैयार करें

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
इस चरण में, आप अपने पहली गिग के लिए मंच तैयार करेंगे और एक रॉक स्टार का नाम चुनेंगे।
</div>
<div>
![](images/set-the-stage.png){:width="300px"}
</div>
</div>

--- task ---

[ड्रम स्टार स्टार्टर प्रोजेक्ट](https://scratch.mit.edu/projects/535783147/editor){:target="_blank"} खोलें। Scratch दूसरे ब्राउज़र टैब में खुलेगा।

[[[working-offline]]]

--- /task ---

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
संगीतकार जिन्हें बुलाया <span style="color: #0faeb0">** DIY कलाकार **</span> बुलाया जाता है उनके बेडरूम से संगीत रिकॉर्डिंग शुरू शुरू करेंगे। वे स्वयं अपने गीत स्वयं बनाते हैं और फिर उन्हें सभी के सुनने के लिए ऑनलाइन रिलीज़ करते हैं। 
</p>

खेल एक DIY कलाकार की तरह एक बेडरूम में शुरू होता है।

--- task ---

**Choose a Backdrop** क्लिक करें और `bedroom` खोजें।

**चुनें:** एक bedroom चुनें और इसे अपने प्रोजेक्ट में जोड़ें। हमने `Bedroom3` चुना।

!['Bedroom 3' की पृष्ठभूमि दिखाने वाला स्टेज।](images/bedroom3.png)

--- /task ---

--- task ---

Scratch में, आप Stage में कोड जोड़ सकते हैं।

Stage पेन से अपने बेडरूम बैकड्रॉप पर क्लिक करें और यह कोड जोड़ें:

![Stage पेन पर पृष्ठभूमि थंबनेल।](images/bedroom-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //आपका बैक्ड्राप (पृष्ठभूमि) नाम
```

--- /task ---

हर संगीतकार को रॉक स्टार का नाम चुनना होता है।

**वेरिएबल (चर)** नंबर और/या टेक्स्ट को स्टोर करने का एक तरीका है। आपका रॉक स्टार नाम `variable`{:class="block3variables"} में संग्रहीत किया जाएगा ताकि इसे किसी भी समय उपयोग किया जा सके।

--- task ---

`Variables`{:class="block3variables"}ब्लॉक मेन्यू से, **Make a Variable** बटन पर क्लिक करें।

इस वेरिएबल को `name` कहें।

![टेक्स्ट इनपुट 'name' के साथ New Variable पॉप अप विंडो।](images/new-variable.png)

**ध्यान दें:** The new `name` चर Stage पर दिखाई देता है और अब `Variable`{:class="block3variables"} ब्लॉक में उपयोग किया जा सकता है।

--- /task ---

--- task ---

प्रोजेक्ट की शुरुआत में, आपके रॉकस्टार का नाम अज्ञात है।

`set name to`{:class="block3variables"} `???` एक ब्लॉक जोड़ें:

![](images/stage-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //आपका बैक्ड्राप (पृष्ठभूमि) नाम
+ set [name v] to [???] //आपका वेरिएबल (चर)
```

--- /task ---

आप Scratch में एक प्रश्न `ask`{:class="block3sensing"} पूछ सकते हैं, फिर एक `variable`{:class="block3variables"} का उपयोग `answer`{:class="block3sensing"} स्टोर करने के लिए कर सकते हैं।

--- task ---

`Sensing`{:class="block3sensing"} ब्लॉक मेनू पर क्लिक करें और अपने कोड में एक `ask`{:class="block3sensing"} ब्लॉक जोड़ें:

![](images/stage-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //आपका बैक्ड्राप (पृष्ठभूमि) नाम
set [name v] to [???] //आपका वेरिएबल (चर)
+ ask [What's your rock star name?] and wait //आपका प्रश्न
```

--- /task ---

--- task ---

`name`{:class="block3variables"} `variable`{:class="block3variables"} को `answer`{:class="block3sensing"}पर सेट करें:

![](images/stage-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //आपका बैक्ड्राप (पृष्ठभूमि) नाम
set [name v] to [???] //आपका वेरिएबल (चर)
ask [What's your rock star name?] and wait //आपका प्रश्न
+ set [name v] to (answer)
```

--- /task ---

आपका `variable`{:class="block3variables"} स्टेज पर कैसा दिखता है उसको बदलें

--- task ---

Stage पर `variable`{:class="block3variables"} पर राइट-क्लिक करें और **large readout** का चयन करें:

![](images/large-readout.png)

--- /task ---

--- task ---

अपने `variable`{:class="block3variables"} को Stage के शीर्ष-दाईं ओर स्थित करने के लिए खींचें:

![](images/repositioned-variable.png)

--- /task ---

--- task ---

**टेस्ट:** यह सुनिश्चित करने के लिए अपना प्रोजेक्ट चलाएं कि`variable`{:class="block3variables"} `???` रूप में शुरू होता है फिर अपने `answer`{:class="block3sensing"} में अपडेट होता है।

--- /task ---

--- task ---

अब जब आपने यह परीक्षण कर लिया है कि `variable`{:class="block3variables"} `answer`{:class="block3sensing"} में बदल जाता है, तो आप कोड के अंतिम 2 ब्लॉक को बाकी स्क्रिप्ट से दूर खींच सकते हैं। इसका मतलब है की आपको हर बार अपना प्रॉजेक्ट टेस्ट करते समय `answer`{:class="block3sensing"} टाइप करने की आवश्यकता नहीं है::

![](images/stage-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //आपका बैक्ड्राप (पृष्ठभूमि) नाम
set [name v] to [???] //आपका वेरिएबल (चर)
```

```blocks3
ask [What's your rock star name?] and wait //आपका प्रश्न
set [name v] to (answer)
```

--- /task ---

--- save ---
