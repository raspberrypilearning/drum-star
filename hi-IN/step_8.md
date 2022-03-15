## प्रोजेक्ट को अपग्रेड करें

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
जैसे जैसे आप और अधिक अद्भुत जगहों पर बजाते हैं अपने प्रोजेक्ट को और अधिक ड्रम और अधिक बैकड्रॉप के साथ अपग्रेड करें। 
</div>
<div>
![](images/upgrade-project.png){:width="300px"}
</div>
</div>

आपके प्रॉजेक्ट में और अधिक अपग्रेड जोड़ने के लिए चुनने के लिए बहुत अधिक ड्रम पोशाकें हैं।

अपग्रेड करने के लिए एक और ड्रम जोड़ने के लिए, प्रोजेक्ट के पिछले चरणों को देखें।

**drum**, के लिए आपको यह करना होगा:

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

**बटन**, के लिए आपको यह करना होगा:

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

`beats`{:class="block3variables"} की संख्या को उससे बदलें जो आपके पास इस ड्रम को पाने के लिए होनी चाहिए `if`{:class="block3events"} कंडीशन में। `beats`{:class="block3variables"} की ऋणात्मक संख्या बदलें `change by`{:class="block3variables"} जब आप इस ड्रम को पाते हैं । `broadcast`{:class="block3events"} प्राप्त करने वाले संदेश **new drum** के नाम से बदलें।

--- /task ---

**venue**, के लिए आपको यह करना होगा:

--- task ---

एक और पृष्ठभूमि जोड़ें।

--- /task ---

--- task ---

जब इस ड्रम के लिए `message`{:class="block3events"} प्राप्त होता है तो नई पृष्ठभूमि में `switch backdrop to`{:class="block3looks"} करने के लिए Stage पर एक स्क्रिप्ट जोड़ें।

--- /task ---

ऐसा हो सकता है की आपको लगे कि आपके ड्रम को एक अलग पृष्ठभूमि पर एक नई स्थिति में होना चाहिए।

--- task ---

हर **drum** स्प्राइट पर `when backdrop changes to`{:class="block3events"} से शुरू होने वाली स्क्रिप्ट जोड़ें और उसके साथ `go to`{:class="block3motion"} ब्लॉक जोड़ें ताकि वह अपनी स्थिति बदलें।

आपको प्रारंभिक स्थिति को `when flag clicked`{:class="block3events"} पर भी सेट करना होगा।

--- /task ---

--- task ---

**सुझाव:** यदि आपके पास समय है, तो यह सुनिश्चित करना एक अच्छा विचार है कि स्प्राइट सूची में स्प्राइट एक तर्कसंगत क्रम में हैं, ड्रम से उनके अपग्रेड क्रम में शुरू होकर और फिर क्रम में बटन।

--- /task ---

--- task ---

**डीबग:** पहले सुनिश्चित करें कि आप वास्तव में समझते हैं कि ड्रम और बटन कब दिखाना चाहिए और `beats`{:class="block3variables"} वेरिएबल कैसे बदलना चाहिए। किसी प्रोजेक्ट को डिबग करना बहुत आसान है यदि आप इस बारे में स्पष्ट हैं कि उसे क्या करना है।

--- collapse ---
---
title: मेरा ड्रम ठीक से दिखाई नहीं देता /छुपाता नहीं है
---

जब तक कि यह पहला ड्रम न हो, आपके ड्रम में `when flag clicked`{:class="block3events"} स्क्रिप्ट होना चाहिए ताकि `hide`{:class="block3looks"}। और इसमे एक `when I receive`{:class="block3events"} `this drum` स्क्रिप्ट होनी चाहिए `show`{:class="block3looks"} के लिए।

जांचें कि इस ड्रम के लिए **Get** बटन एक ही संदेश `broadcasts`{:class="block3events"} करे।


--- /collapse ---

--- collapse ---
---
title: मेरा Get बटन सही ढंग से दिखाई नहीं देता /छुपाता नहीं है
---

जब तक बटन पहले ड्रम के लिए न हो, तब इसे `hide`{:class="block3looks"} `when flag clicked`{:class="block3events"}। और इसे **previous drum** के लिए संदेश `show`{:class="block3looks"} `when I receieve`{:class="block3events"} होना चाहिए। **Get** बटन को खिलाड़ी को अगले अपग्रेड के बारे में बताने के लिए जिस पर वे काम कर रहे हैं `show`{:class="block3looks"} चाहिए।

--- /collapse ---

--- collapse ---
---
title: जब मेरे पास पर्याप्त बीट्स न हों तो मैं ड्रम खरीद सकता हूं
---

जब ड्रम के लिए **Get**बटन स्क्रिप्ट `when this sprite clicked`{:class="block3events"} तो जाँचें की आपने जितनी ज़रूरत हो उतनी `beats`{:class="block3variables"} बदली हैं ।

--- /collapse ---

--- collapse ---
---
title: जब मैं एक नया ड्रम प्राप्त करता हूं तो बीट्स की संख्या सही ढंग से नहीं बदलती है
---

जब ड्रम के लिए **Get**बटन स्क्रिप्ट `when this sprite clicked`{:class="block3events"} तो जाँचें कीआपने `changed beats by`{:class="block3variables"}को एक ऋणात्मक संख्या में बदला है।

सुनिश्चित करें कि यह ड्रम बटन पोशाक पर संख्या से मेल खाता है।

--- /collapse ---

--- /task ---

--- collapse ---
---
title: पूरा किया हुआ प्रोजेक्ट।
---

आप [ पूर्ण प्रोजेक्ट यहां से प्राप्त कर सकते हैं ](https://scratch.mit.edu/projects/660058523/){:target="_blank"}.

--- /collapse ---

**सुझाव:** यदि आप वास्तव में अव्यवस्थित हो जाते हैं तो नया ड्रम और उसके बटन को हटाना ठीक है, और फिर से शुरू करें। कभी-कभी बग का पता लगाना मुश्किल होता है।

--- save ---
