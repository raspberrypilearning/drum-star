
--- question ---

---
legend: Question 3 of 3
---

प्लेयर त्यांचा ड्रम अपग्रेड करण्यासाठी बटनवर क्लिक करतो तेव्हा काय घडते ते नियंत्रीत करण्यासाठी तुम्ही ही स्क्रिप्ट वापरली:

```blocks3
when this sprite clicked
if <(beats)>  [29]> then 
hide
change [beats v] by [-30] 
broadcast (conga v) 
else
say [Not enough beats!] for [2] seconds 
end
```

`beats`{:class="block3variables"} व्हेरिएबलची व्हॅल्यू `29` असल्यास, प्लेयरने बटनवर क्लिक केल्यावर काय घडेल?

--- choices ---

- ( ) sprite `hide`{:class="block3looks"} होईल

  --- feedback ---

  अगदीच नाही, स्क्रिप्टमध्ये `hide`{:class="block3looks"} ब्लॉक आहे, परंतु तो `29` `beats`{:class="block3variables"} सह रन होईल. स्क्रिप्ट पुन्हा एकदा पहा.

  --- /feedback ---

- (x) बटन स्प्राईटला `say`{:class="block3looks"} `Not enough beats!`

  --- feedback ---

हो, स्थिती तपासते की `beats`{:class="block3variables"} हे `29` पेक्षा मोठे आहे का, परंतु `beats`{:class="block3variables"} हे `29` च्या बरोबर आहे त्यामुळे प्लेयरकडे पुरेसे नाही.

  --- /feedback ---

- `beats`{:class="block3variables"} व्हेरिएबलच्या व्हॅल्यूमधून ( ) 30 काढून घेतले जाईल

  --- feedback ---

  नाही, `beats`{:class="block3variables"} ची व्हॅल्यू सारखीच राहील. `beats`{:class="block3variables"} म्हणजे `29` आहे ज्याचा अर्थ असा की, `beats`{:class="block3variables"} `> 29` चूक आहे, त्यामुळे `if`{:class="block3control"} ब्लॉकच्या पहिल्या भागातील ब्लॉक्स रन होणार नाहीत.

  --- /feedback ---

- ( ) काहीही नाही

  --- feedback ---

  नाही, स्क्रिप्ट नेहमी काहीतरी करेल. तुमच्याकडे `29` `beats`{:class="block3variables"} असल्यावर स्क्रिप्टचा कोणता भाग रन होईल हे बघण्यासाठी जवळून बघा.

  --- /feedback ---

--- /choices ---

--- /question ---
