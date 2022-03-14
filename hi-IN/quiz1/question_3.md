
--- question ---

---
legend: 3 में से तीसरा प्रश्न
---

आपने इस स्क्रिप्ट का उपयोग यह नियंत्रित करने के लिए किया है कि जब खिलाड़ी अपने ड्रम को अपग्रेड करने के लिए बटन पर क्लिक करता है तो क्या होता है:

```blocks3
when this sprite clicked
if <(beats)>  [29]> then 
hide
change [beats v] by [-30] 
broadcast [conga v] 
else
say [Not enough beats!] for [2] seconds 
end
```

यदि `beats`{:class="block3variables"} वेरिएबल का मान `29` है, तो खिलाड़ी द्वारा बटन पर क्लिक करने पर क्या होगा?

--- choices ---

- ( ) स्प्राइट `hide`{:class="block3looks"}

  --- feedback ---

  पूरी तरह से नहीं, `hide`{:class="block3looks"} स्क्रिप्ट में एक ब्लॉक है लेकिन यह `29` `beats`{:class="block3variables"} के साथ नही चलेगा । एक बार फिर से स्क्रिप्ट पर एक नजर डालें।

  --- /feedback ---

- (x) बटन स्प्राइट `say`{:class="block3looks"} `Not enough beats!`

  --- feedback ---

हां, अगर से `beats`{:class="block3variables"} `29` से बड़ी है शर्त पूरी होती है, लेकिन `beats`{:class="block3variables"} `29` के बराबर है ताकि खिलाड़ी के पास पर्याप्त नहीं है।

  --- /feedback ---

- `beats`{:class="block3variables"} वेरिएबल के मान से ( ) 30 हटा दिया जाएगा

  --- feedback ---

  नहीं, `beats`{:class="block3variables"} वेरिएबल का मान वही रहेगा। `beats`{:class="block3variables"} `29` है जिसका अर्थ है `beats`{:class="block3variables"} `> 29` ग़लत है, ताकि `if`{:class="block3control"} के पहले भाग में ब्लॉक नहीं चलेगा।

  --- /feedback ---

- ( ) कुछ भी नहीं

  --- feedback ---

  नहीं, स्क्रिप्ट हमेशा कुछ न कुछ करेगी। जब आपके पास `29` `beats`{:class="block3variables"} हो, तो स्क्रिप्ट का कौन सा भाग चलेगा, यह देखने के लिए करीब से देखें।

  --- /feedback ---

--- /choices ---

--- /question ---
