## प्रथम अपग्रेड

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
तुम्ही तुमचे पहिले अपग्रेड जोडाल. **Get snare** बटन सुरूवातील दाखवेल, ज्यामुळे प्लेयरला माहिती असेल की ते कोणत्या ड्रमसाठी कार्य करत आहेत.
</div>
<div>
![](images/first-upgrade.png){:width="300px"}
</div>
</div>

--- task ---

तुमच्या प्रोजेक्टमध्ये **Drum-snare** स्प्राईट जोडा आणि तो Stage वर पोजिशन करा:

![](images/snare-stage.png)

--- /task ---

--- task ---

`when this sprite clicked`{:class="block3events"} स्क्रिप्ट **Drum-cymbal** स्प्राईटमधून **Drum-snare** स्प्राईटला ड्रॅग करा.

[[[scratch3-copy-code]]]

--- /task ---

--- task ---

कॉश्चुम आणि ड्रम साऊंड बदला.

बीट्सची मिळवलेली संख्या `2` ला बदला:

![](images/snare-icon.png)

```blocks3
when this sprite clicked
+change [beats v] by [2] //प्रती क्लिक 2 बीट्स
+switch costume to [drum-snare-b v] //हिट कॉश्चुम
+play drum [(1) Snare Drum v] for [0.25] beats //ड्रम साऊंड
+switch costume to [drum-snare-a v] //नॉट हिट कॉश्चुम
```

--- /task ---

--- task ---

**चाचणी:** तुमच्या प्रोजेक्टचा प्रयत्न करा. तुम्ही snare ड्रमवर क्लिक केल्यावर तुम्हाला 2 बीट्स मिळाल्याची खात्री करा.

--- /task ---

तुम्ही प्रोजेक्ट सुरू केल्यावर अपग्रेड्स उपलब्ध नाहीत. त्यांनी बीट्स मिळवायला हवे.

--- task ---

प्रोजेक्टच्या सुरूवातीला हा **drum** स्प्राईट लपवण्यासाठी स्क्रिप्ट जोडा:

![](images/snare-icon.png)

```blocks3
when flag clicked
hide
```

--- /task ---

कोणता ड्रम पुढील अपग्रेड पर्याय आणि किती बीट्सला किंमत आहे हे बटन दाखवेल.

--- task ---

**Get** स्प्राईट **Duplicate** करा:

![](images/duplicate-get.png)

**Show** ला व्हिजीबिलीटी बदला आणि त्याचे नाव `Get snare` असे बदला. Stage च्या खालच्या उजव्या कोपऱ्यात त्याला पोजिशन करा:

![](images/get-snare.png)

--- /task ---

--- task ---

**Drum-snare** स्प्राईटवर क्लिक करा आणि **Costumes** टॅबवर क्लिक करा. तुमच्या ड्रमचा नॉट हिट कॉश्चुम हायलाईट करण्यासाठी **Select** (ऍरो) टूल वापरा. **Group** आयकॉनवर क्लिक करा त्यानंतर **Copy** आयकॉनवर क्लिक करा:

![](images/snare-icon.png)

![](images/copy-costume.png)

--- /task ---

--- task ---

तुमच्या **Get snare** स्प्राईटवर क्लिक करा आणि snare कॉश्चुम **Paste** करा. तुम्ही कदाचीत रीसाईज करण्याची आणि तुमचे बटन फिट करण्यासाठी ते पोजीशन करण्याची आवश्यकता असू शकते:

![](images/get-snare-icon.png)

![](images/paste-costume.png)

--- /task ---

--- task ---

**Code** टॅबवर क्लिक करा आणि प्रोजेक्टच्या सुरूवातीला **Get snare** स्प्राईट दाखवण्यासाठी स्क्रिप्ट जोडा:

![](images/get-snare-icon.png)

```blocks3
when flag clicked
show
```

--- /task ---

यूजरकडे `10` किंवा अधिक बीट्स असल्यासच केवळ अपग्रेड खरेदी केले जाऊ शकते. [ड्रॅगनफ्लाय वाढवा](https://projects.raspberrypi.org/mr-IN/projects/grow-a-dragonfly){:target="_blank"} मध्ये, तुम्ही `if`{:class="block3control"} ब्लॉक्ससह निर्णय घेण्याबद्दल शिकलात.

`if ... else`{:class="block3control"} ब्लॉक निर्णय घेण्यासाठी वापरला जातो आणि स्थिती `बरोबर` किंवा `चूक` असल्यास वेगवेगळ्या गोष्टी केल्या जातील.

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
सर्ववेळी निर्णय घेण्यासाठी आपण <span style="color: #0faeb0">**if ... else**</span> वापरतो. तुम्ही उठता तेव्हा, तुम्ही तपासता `if`{:class="block3control"} सकाळ आहे का. तुम्ही उठता, किंवा `else`{:class="block3control"} तुम्ही परत झोपी जाता. तुम्ही घेतलेल्या कोणत्या `if ... else`{:class="block3control"} निर्णयाबद्दल तुम्ही विचार करू शकता का? 
</p>

--- task ---

`if`{:class="block3control"} प्लेयरकडे पुरेसे बीट्स असले, किंवा जर ते अपग्रेड करण्यास सक्षम नसल्यावर `say`{:class="block3looks"} `Not enough beats!` तर अपग्रेड मिळवण्यासाठी हा कोड जोडा:

![](images/get-snare-icon.png)

```blocks3
when this sprite clicked
if <(beats)>  [9]> then //10 किंवा अधिक बीट्स असल्यास
hide
change [beats v] by [-10] //मूल्य अपग्रेड काढून घ्या
else
say [Not enough beats!] for [2] seconds 
end
```

--- /task ---

इतर स्प्राईट्स आणि Stage ला snare अपग्रेड खरेदी केल्या गेला हे माहिती होऊ द्या.

--- task ---

नवीन `snare` मेसेज पाठवण्यासाठी `broadcast`{:class="block3events"} ब्लॉक जोडा:

![](images/get-snare-icon.png)

```blocks3
when this sprite clicked
if <(beats)>  [9]> then // 10 किंवा अधिक बीट्स असल्यास
hide
change [beats v] by [-10] // मूल्य अपग्रेड काढून घ्या
+ broadcast [snare v] // तुमच्या ड्रमचे नाव
else
say [Not enough beats!] for [2] seconds 
end
```

--- /task ---

--- task ---

**Drum-snare** स्प्राईटवर क्लिक करा. ही स्क्रिप्ट जोडा:

![](images/snare-icon.png)

```blocks3
when I receive [snare v]
show
```

--- /task ---

तुम्ही तुमचे उपकरण अपग्रेड केल्यावर, तुम्ही मोठ्या ठिकाणी प्ले करण्यास सक्षम व्हाल.

--- task ---

दुसरा बॅकड्रॉप जोडा. आम्ही शाळेत आमचा दुसरा गिग प्ले करण्यासाठी **Chalkboard** निवडला.

अपग्रेड मेसेज प्राप्त झाल्यावर `switch backdrop`{:class="block3looks"} ला Stage वर कोड जोडा:

![](images/stage-icon.png)

```blocks3
when I receive [snare v]
switch backdrop to [Chalkboard v]
```

**टीप:** बेडरूममधून लहान पायरीवर असलेले ठिकाण निवडा. तुम्हाला नंतरसाठी मोठे ठिकाण सेव करायचे आहे.

--- /task ---

--- task ---

**चाचणी:** तुमचा प्रोजेक्ट रन करा. तुमच्याकडे पुरेसे बीट्स असण्याआधी snare अपग्रेडसाठी प्रयत्न करा आणि खरेदी करा.

तुम्ही अपग्रेड चेक खरेदी करता तेव्हा: snare दिसतो, बटन नाहीसे होते, ठिकाण बदलते आणि `beats`{:class="block3variables"} `10` ने कमी होतात.

--- /task ---

--- save ---
