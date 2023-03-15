
--- question ---

---
legend: السؤال 2 من 3
---

يحتوي المشروع على هذا البرنامج النصي ليسأل المستخدم عن اسمه:

```blocks3
when flag clicked
set [الاسم v] to [???] 
ask [ما هو اسمك؟] and wait 
set [الاسم v] to (answer)
```

![](images/q1-chatbot.png)

ماذا ستكون قيمة المتغير `الاسم`{:class="block3variables"} بعد أن ينقر المستخدم على علامة الاختيار (علامة الاختيار) وينتهي المقطع البرمجي؟

--- choices ---

- ( ) اسم

  --- feedback ---

لا ، `الاسم`{:class="block3variables"} هو ما يسمى المتغير.

  --- /feedback ---

- () ؟؟؟

  --- feedback ---

لا `؟؟؟` هي قيمة متغير `الاسم`{:class="block3variables"} قبل تنفيذ المقطع البرمجي `اسال`{:class="block3sensing"}.

  --- /feedback ---

- ( ) إجابة

  --- feedback ---

لا ، `إجابة`{:class="block3sensing"} هو المتغير المضمن الذي يستخدمه Scratch لتخزين اجابتك عندما `تسال`{:class="block3sensing"} سؤالاً.
  --- /feedback ---

(x) Bobo

--- feedback ---


نعم ، عيّن `اجعل [الاسم v] إلى`{:class="block3variables"} القيمة من`الاسم`{:class="block3variables"} متغير على قيمة`الاجابة`{:class="block3sensing"} وهو النص الذي أدخله المستخدم.

سيتم أيضًا عرض القيمة `Bobo` على المسرح.

  --- /feedback ---

--- /choices ---

--- /question ---
