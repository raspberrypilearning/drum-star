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

--- /task ---

The drummer starts in a bedroom like a beginner!

--- task ---

**Choose a Backdrop** क्लिक करें और `bedroom` खोजें।

Select a bedroom and add it to your project. हमने `Bedroom3`चुना।

!['Bedroom 3' की पृष्ठभूमि दिखाने वाला स्टेज।](images/bedroom3.png)

--- /task ---

Scratch में, आप Stage में कोड जोड़ सकते हैं।

--- task ---

Stage पेन से अपने बेडरूम बैकड्रॉप पर क्लिक करें और यह कोड जोड़ें:

![Stage पेन पर पृष्ठभूमि थंबनेल।](images/bedroom-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //your backdrop name
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
switch backdrop to (Bedroom 3 v) //your backdrop name
+ set [name v] to [???] //your variable
```

--- /task ---

आप Scratch में एक प्रश्न `ask`{:class="block3sensing"} पूछ सकते हैं, फिर एक `variable`{:class="block3variables"} का उपयोग `answer`{:class="block3sensing"} स्टोर करने के लिए कर सकते हैं।

--- task ---

`Sensing`{:class="block3sensing"} ब्लॉक मेनू पर क्लिक करें और अपने कोड में एक `ask`{:class="block3sensing"} ब्लॉक जोड़ें:

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //your backdrop name
set [name v] to [???] //your variable
+ ask [What's your rock star name?] and wait //your question
```

--- /task ---

--- task ---

`name`{:class="block3variables"} `variable`{:class="block3variables"} को `answer`{:class="block3sensing"}पर सेट करें:

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //your backdrop name
set [name v] to [???] //your variable
ask [What's your rock star name?] and wait //your question
+ set [name v] to (answer)
```

--- /task ---

--- task ---

Stage पर `variable`{:class="block3variables"} पर राइट-क्लिक करें और **large readout** का चयन करें:

![](images/large-readout.png)

--- /task ---

--- task ---

Drag your `variable`{:class="block3variables"} to position it top-right of the Stage:

![](images/repositioned-variable.png)

--- /task ---

--- task ---

**टेस्ट:** यह सुनिश्चित करने के लिए अपना प्रोजेक्ट चलाएं कि`variable`{:class="block3variables"} `???` रूप में शुरू होता है फिर अपने `answer`{:class="block3sensing"} में अपडेट होता है।

--- /task ---

You don't want to type an answer every time you test your project.

--- task ---

Drag the last two blocks of code away from the rest of the script.

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) //your backdrop name
set [name v] to [???] //your variable
```

```blocks3
ask [What's your rock star name?] and wait //your question
set [name v] to (answer)
```

--- /task ---

--- save ---
