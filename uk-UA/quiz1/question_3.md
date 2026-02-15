
--- question ---

---
legend: Question 3 of 3
---

Цей скрипт визначає, що відбувається, коли гравець натискає кнопку отримання нового барабана:

```blocks3
when this sprite clicked
if <(удари)>  [29]> then 
hide
change [удари v] by [-30] 
broadcast (конґа v) 
else
say [Недостатньо ударів!] for [2] seconds 
end
```

Якщо значення змінної `удари`{:class="block3variables"} буде`29`, що станеться, коли гравець натисне на кнопку?

--- choices ---

- () Спрайт `сховається`{:class="block3looks"}

  --- feedback ---

  Не зовсім так. У скрипті є блок `сховати`{:class="block3looks"}, але він не працюватиме з `29` `ударами`{:class="block3variables"}. Поглянь ще раз на скрипт.

  --- /feedback ---

- (x) Спрайт кнопки `скаже`{:class="block3looks"} `Недостатньо ударів!`

  --- feedback ---

Так. Умова перевіряє, чи значення `ударів`{:class="block3variables"} перевищує `29`, але змінна `удари`{:class="block3variables"} дорівнює `29`, тому гравцеві недостатньо ударів.

  --- /feedback ---

- () 30 буде вилучено зі значення змінної `удари`{:class="block3variables"}

  --- feedback ---

  Ні, значення змінної `удари`{:class="block3variables"} залишиться незмінним. Значення змінної `удари`{:class="block3variables"} становить `29`, що означає `удари`{:class="block3variables "} `> 29` є помилковим. Тому блоки в першій частині блоку `якщо`{:class="block3control"} не будуть працювати.

  --- /feedback ---

- () Нічого

  --- feedback ---

  Ні, скрипт буде завжди щось робити. Визнач, яка частина скрипту запуститься, коли у тебе `29` `ударів`{:class="block3variables"}.

  --- /feedback ---

--- /choices ---

--- /question ---
