## तुमचा प्रोजेक्ट अपग्रेड करा

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
तुम्ही अधिक आश्चर्यकारक ठिकाणी खेळलात त्यामुळे अधिक ड्रम आणि अधिक बॅकड्रॉपसह तुमचा प्रोजेक्ट अपग्रेड करा. 
</div>
<div>
![](images/upgrade-project.png){:width="300px"}
</div>
</div>

तुमच्या प्रोजेक्टला आणखी अपग्रेड्स जोडण्यासाठी निवड करावी असे बरेच ड्रम कॉश्चुम आहेत.

अपग्रेडसाठी दुसरा ड्रम जोडण्यासाठी, प्रोजेक्टच्या आधीचे टप्पे बघा.

**drum** साठी, तुम्हाला आवश्यकता असेल:

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

**बटन** साठी, तुम्हाला यासाठी आवश्यकता असेल:

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

`beats`{:class="block3variables"} ची संख्या बदला तुम्ही हा ड्रम `if`{:class="block3events"} स्थितीत मिळवायला हवा. तुम्ही हा ड्रम मिळवता त्यावेळी तुम्ही `change by`{:class="block3variables"} केलेल्या `beats`{:class="block3variables"} ची ऋण संख्या बदला. Change the number that `beats`{:class="block3variables"} needs to be subtracted from in the `join`{:class="block3operators"} block. Change the message that gets `broadcast`{:class="block3events"} to the name of the **new drum**.

--- /task ---

**ठिकाणासाठी**, तुम्हाला याची आवश्यकता आहे:

--- task ---

नवीन बॅकड्रॉप जोडणे.

--- /task ---

--- task ---

या ड्रमसाठी `message`{:class="block3events"} प्राप्त झाल्यावर `switch backdrop to`{:class="block3looks"} या नवीन बॅकड्रॉपला Stage ला स्क्रिप्ट जोडा.

--- /task ---

तुमचे ड्रम वेगवेगळ्या बॅकड्रॉपवर नवीन पोजिशन मध्ये असण्याची आवश्यकता तुम्हाला कदाचीत जाणवेल.

--- task ---

Add a script starting with `when backdrop changes to`{:class="block3events"} to each **drum** sprite with a `go to`{:class="block3motion"} block to make them change position.

तुम्ही त्यांची सुरूवातीची पोजिशन सुद्धा सेट कराल `when flag clicked`{:class="block3events"}.

--- /task ---

--- task ---

**नीटनेटका:** तुमच्याकडे वेळ असल्यावर, स्प्राईट लीस्टमधील स्प्राईट्स अर्थपूर्ण क्रमात असणे ही उत्तम कल्पना आहे, ड्रमपासून त्यांच्या अपग्रेड ऑर्डरने सुरूवात करावी आणि त्यानंतर बटन क्रमात लावावेत.

--- /task ---

--- task ---

**डीबग:** ड्रम्स आणि बटन्सने दाखवायला हवे आणि `beats`{:class="block3variables"} व्हेरिएबल बदलायला हवा हे खरोखर तुम्हाला समजले असल्याची खात्री करा. काय करायला हवे हे तुम्हाला स्पष्ट असल्यास प्रोजेक्ट डीबग करणे फार सोपे आहे.

--- collapse ---
---
title: माझा ड्रम योग्यपणे दाखवत नाही/लपवत नाही
---

तो पहिला ड्रम असल्याशिवाय, तुमच्या ड्रमला `hide`{:class="block3looks"} करण्यासाठी `when flag clicked`{:class="block3events"} स्क्रिप्ट असायला हवी. आणि त्याला `show`{:class="block3looks"} साठी `when I receive`{:class="block3events"} `this drum` स्क्रिप्ट असायला हवी.

या ड्रमसाठी **Get** बटन सारखाच मेसेज `broadcasts`{:class="block3events"} करतो का ते तपासा.


--- /collapse ---

--- collapse ---
---
title: माझे Get बटन योग्यपणे दाखवत नाही/लपवत नाही
---

बटन फार पहिल्या ड्रमसाठी असल्याशिवाय, ते `hide`{:class="block3looks"} `when flag clicked`{:class="block3events"}. And it should `show`{:class="block3looks"} `when I receive`{:class="block3events"} the message for the **previous drum**. **Get** बटन प्लेयरला ते कार्य करत असलेल्या पुढील अपग्रेडबद्दल माहिती असण्यासाठी `show`{:class="block3looks"} हवे.

--- /collapse ---

--- collapse ---
---
title: माझ्याकडे पुरेसे बीट्स नसतांना मी ड्रम खरेदी करू शकतो
---

ड्रमसाठी **Get** बटन साठी स्क्रिप्ट मधील `when this sprite clicked`{:class="block3events"} आवश्यकता असल्यास `beats`{:class="block3variables"} ची संख्या तुम्ही बदललीत का ते तपासा.

--- /collapse ---

--- collapse ---
---
title: मला नवीन ड्रम मिळाल्यावर बीट्सची संख्या योग्यपणे बदलली नाही
---

तुम्ही ड्रमसाठी **Get** बटनसाठी स्क्रिप्ट मधील `when this sprite clicked`{:class="block3events"}ऋण संख्या `changed beats by`{:class="block3variables"} केलीत का ते तपासा.

यामुळे ड्रम बटन कॉश्चुमवरील संख्या जुळते याची खात्री करा.

--- /collapse ---

--- /task ---

--- collapse ---
---
title: पूर्ण झालेला प्रोजेक्ट
---

तुम्ही [पूर्ण झालेला प्रोजेक्ट येथे](https://scratch.mit.edu/projects/522323676/){:target="_blank"} बघू शकता.

--- /collapse ---

**टीप:** जर तुम्ही खरोखर गोंधळले असाल तर नवीन ड्रम आणि त्याचे बटण डिलीट करणे आणि पुन्हा सुरू करणे योग्य आहे. काहीवेळा त्रुटी शोधणे कठीण असते.

--- save ---
