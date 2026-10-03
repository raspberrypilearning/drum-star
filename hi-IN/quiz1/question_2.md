
--- question ---

---
legend: Question 2 of 3
---

एक प्रोजेक्ट में यह स्क्रिप्ट `ask`{:class="block3sensing"} उपयोगकर्ता को उनके नाम के लिए है:

```blocks3
when flag clicked
set [name v] to [???] 
ask [What's your name?] and wait 
set [name v] to (answer)
```

![](images/q1-chatbot.png)

खिलाड़ी द्वारा टिक (चेकमार्क) पर क्लिक करने और स्क्रिप्ट समाप्त होने के बाद `name`{:class="block3variables"} वेरिएबल का मान क्या होगा?

--- choices ---

- ( ) नाम

  --- feedback ---

नहीं, वेरिएबल `name`{:class="block3variables"} कहलाता है।

  --- /feedback ---

- ( ) ???

  --- feedback ---

नहीं, `ask`{:class="block3sensing"} ब्लॉक चलने से पहले `???` `name`{:class="block3variables"} वेरिएबल का मान है।

  --- /feedback ---

- ( ) उत्तर

  --- feedback ---

नहीं, `answer`{:class="block3sensing"} बिल्ट-इन वेरिएबल है जिसका उपयोग Scratch उस उत्तर को स्टोर करने के लिए करता है जिसे उपयोगकर्ता टाइप करता है जब आप प्रश्न `ask`{:class="block3sensing"} हैं। --- /feedback ---

- (x) Bobo

  --- feedback ---

हां, `set [name v] to`{:class="block3variables"} ब्लॉक `name`{:class="block3variables"} वेरिएबल को **value** `answer`{:class="block3sensing"} के मान पर सेट करता है जो वह टेक्स्ट है जिसे उपयोगकर्ता ने दर्ज किया है।

`Bobo` का मान भी भी Stage पर दिखाया जाएगा।

  --- /feedback ---

--- /choices ---

--- /question ---
