
--- question ---

---
legend: Питання 2 з 3
---

У проєкті є цей скрипт, який `запитує`{:class="block3sensing"} користувача, як його звуть:

```blocks3
when flag clicked
set [імʼя v] to [???] 
ask [Як тебе звуть?] and wait 
set [імʼя v] to (answer)
```

![](images/q1-chatbot.png)

Яким буде значення змінної `ім'я`{:class="block3variables"} після того, як гравець натисне галочку і скрипт завершиться?

--- choices ---

- () ім'я

  --- feedback ---

Ні, `ім’я`{:class="block3variables"} – це назва змінної.

  --- /feedback ---

- () ???

  --- feedback ---

Ні, `???` — це значення змінної `ім'я`{:class="block3variables"} до того, як виконається блок `запитати`{:class="block3sensing"}.

  --- /feedback ---

- () відповідь

  --- feedback ---

Ні, `відповідь`{:class="block3sensing"} – це вбудована змінна, яку Скретч використовує для зберігання відповіді, що її вводить користувач, коли його щось `запитують`{:class=" block3sensing"}. --- /feedback ---

- (x) Бобо

  --- feedback ---

Так, блок `надати [ім'я v] значення`{:class="block3variables"} надає змінній `ім'я`{:class=" block3variables"} **значення** змінної `відповідь`{:class="block3sensing"}, введене користувачем.

Значення `Бобо` також буде показано на сцені.

  --- /feedback ---

--- /choices ---

--- /question ---
