
--- question ---

---
legend: Question 2 of 3
---

यूजरला त्यांचे नाव `ask`{:class="block3sensing"} साठी प्रोजेक्टला ही स्क्रिप्ट आहे:

```blocks3
when flag clicked
set [name v] to [???] 
ask [What's your name?] and wait 
set [name v] to (answer)
```

![](images/q1-chatbot.png)

प्लेयरने टीक (चेकमार्क) वर क्लिक केल्यावर आणि स्क्रिप्ट संपल्यावर `name`{:class="block3variables"} ची व्हॅल्यू काय असेल?

--- choices ---

- () नाव

  --- feedback ---

नाही, `name`{:class="block3variables"} हे व्हेरिएबलला म्हणतात.

  --- /feedback ---

- ( ) ???

  --- feedback ---

नाही, `ask`{:class="block3sensing"} ब्लॉक रन करण्याआधी `name`{:class="block3variables"} व्हेरिएबलची `???` ही व्हॅल्यू आहे.

  --- /feedback ---

- () उत्तर

  --- feedback ---

नाही, `answer`{:class="block3sensing"} हा बिल्ट-इन व्हेरिएबल आहे जो Scratch प्रश्न `ask`{:class="block3sensing"} जातो त्यावेळी यूजरने टाईप केलेले उत्तर स्टोअर करण्यासाठी वापरतो. --- /feedback ---

- (x) Bobo

  --- feedback ---

हो, </code>{:class="block3variables"} ब्लॉकला `set [name v] करण्यासाठी <code>name`{:class="block3variables"} ची **value** ही `answer`{:class="block3sensing"} च्या व्हॅल्यूला सेट करा जी यूजरने एंटर केलेले टेक्स्ट असेल.

`Bobo` ची व्हॅल्यू Stage वर सुद्धा दाखवली जाईल.

  --- /feedback ---

--- /choices ---

--- /question ---
