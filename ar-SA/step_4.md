## التطوير الاول

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
سوف تضيف الترقية او التطوير الأول الخاصة بك. سيظهر زر ** الحصول على snare ** في البداية ، حتى يعرف اللاعب الطبلة التي يعمل عليها.
snare نوع من انواع الطبل.
</div>
<div>
![](images/first-upgrade.png){:width="300px"}
</div>
</div>

--- task ---

أضف الكائن **Drum-snare** إلى مشروعك وقم بوضعه على المنصة:

![](images/snare-stage.png)

--- /task ---

--- task ---

اسحب المقطع البرمجي `عند النقر على هذا الكائن`ن {: class = "block3events"} من **Drum-cymbal** sprite إلى كائن **Drum-snare**.

[[[scratch3-copy-code]]]

--- /task ---

--- task ---

تغيير المظاهر وصوت الطبل.

قم بتغيير عدد الدقات التي حصلت عليه إلى `2`:

![](images/snare-icon.png)

```blocks3
when this sprite clicked
+change [beats v] by [2] //2 beats per click
+switch costume to [drum-snare-b v] //hit costume
+play drum [(1) Snare Drum v] for [0.25] beats //drum sound
+switch costume to [drum-snare-a v] //not hit costume
```

--- /task ---

--- task ---

**اختبار:** قم بتجربة مشروعك. تأكد من حصولك على دقاتين عند النقر على طبلة snare.

--- /task ---

الترقيات غير متوفرة عند بدء المشروع. يجب أن يكتسبوا بالضربات الى الطبل.

--- task ---

أضف مقطع برمجي لإخفاء هذا الكائن **drum** في بداية المشروع:

![](images/snare-icon.png)

```blocks3
when flag clicked
hide
```

--- /task ---

سيظهر الزر أي طبل هي من الخيارات التالية للترقية وعدد الإيقاعات التي ستكلفها.

--- task ---

**مضاعفة** ، **، احصل على** مظهر:

![](images/duplicate-get.png)

قم بتغيير حالة الاظهار إلى **اظهار** وقم بتغيير اسمه إلى `Get snare`. وقم بوضعه في الركن الأيمن السفلي من المنصة:

![](images/get-snare.png)

--- /task ---

--- task ---

انقر فوق كائن **Drum-snare** وانتقل إلى علامة التبويب **المظاهر**. استخدم أداة **تحديد** (السهم) لتحديد الكائن بالكامل. انقر على أيقونة **تجمع** ثم أيقونة **نسخ**:

![](images/snare-icon.png)

![](images/copy-costume.png)

--- /task ---

--- task ---

انقر على **الحصول على snare ** و **لصق** مظهر الــ snare  . قد تحتاج إلى تغيير حجمه وl,rui ليلائم الزر الخاص بك:

![](images/get-snare-icon.png)

![](images/paste-costume.png)

--- /task ---

--- task ---

انقر فوق علامة التبويب **المقطاع البرمجية** وأضف مقطع برمجي لاظهار الكائن **Get snare** في بداية المشروع:

![](images/get-snare-icon.png)

```blocks3
when flag clicked
show
```

--- /task ---

يمكن شراء الترقية فقط إذا كان لدى المستخدم `10` نبضة أو أكثر. في مشروع[نمو اليعسوبب](https://projects.raspberrypi.org/en/projects/grow-a-dragonfly){: target = "_ blank"} ، تعلمت كيفية اتخاذ القرارات باستخدام المقطع البرمجي `اذا`{: class = "block3control"}.

يتم استخدام المقطع البرمجي `اذا ... والا`{: class = "block3control"} لاتخاذ قرار وستقوم بأشياء مختلفة إذا كان الشرط `صحيحًا` أو `خطأ`.

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
نستخدم <span style="color: #0faeb0">** اذا ... والا **</span> طوال الوقت لاتخاذ القرارات. عندما تستيقظ ، تتحقق من `اذا` {: class =" block3control "} هذا الصباح. استيقظ ، أو `والا` {: class =" block3control "} تعود للنوم. هل يمكنك التفكير في أي قرارات تتخذها بشأن "اذا ... else" {: والا = "block3control"}؟ 
</p>

--- task ---

Add this code to get the upgrade `if`{:class="block3control"} the player has enough beats, or `say`{:class="block3looks"} `More beats needed!` if they are not able to upgrade:

![](images/get-snare-icon.png)

```blocks3
when this sprite clicked
if <(beats)>  [9]> then //if 10 or more beats
hide
change [beats v] by [-10] //take away the cost of upgrade
else
say [More beats needed!] for [2] seconds 
end
```

--- /task ---

Instead of only telling the player they need **more** beats, you can tell the player exactly **how many more** beats are needed to get the upgrade.

A `join`{:class="block3operators"} block is used to concatenate, or 'link' two values together.

![](images/get-snare-icon.png)

--- task ---

Add this code to `join`{:class="block3operators"} the number of beats needed with the text you have used to tell the player they need more beats if they are not able to upgrade:

```blocks3
when this sprite clicked
if <(beats)>  [9]> then //if 10 or more beats
hide
change [beats v] by [-10] //take away the cost of upgrade
else
+ say (join ((10) - (beats)) [beats needed!]) for [2] seconds
end
```

--- /task ---

--- task ---

Add a `broadcast`{:class="block3events"} block to send a new `snare` message:

![](images/get-snare-icon.png)

```blocks3
when this sprite clicked
if <(beats)>  [9]> then // if 10 or more beats
hide
change [beats v] by [-10] // take away the cost of upgrade
+ broadcast [snare v] // your drum name
else
say (join ((10) - (beats)) [beats needed!]) for [2] seconds
end
```

--- /task ---

--- task ---

Click on the **Drum-snare** sprite. Add this script:

![](images/snare-icon.png)

```blocks3
when I receive [snare v]
show
```

--- /task ---

When you upgrade your equipment, you will be able to play at bigger venues.

--- task ---

Add another backdrop. We chose **Chalkboard** to play our second gig at school.

Add code to the Stage to `switch backdrop`{:class="block3looks"} when the upgrade message is received:

![](images/stage-icon.png)

```blocks3
when I receive [snare v]
switch backdrop to [Chalkboard v]
```

**Tip:** Choose a venue that's a small step up from the bedroom. You want to save bigger venues for later.

--- /task ---

--- task ---

**Test:** Run your project. Try and buy the snare upgrade before you have enough beats.

When you buy the upgrade check: the snare appears, the button disappears, the venue changes and the `beats`{:class="block3variables"} go down by `10`.

--- /task ---

--- save ---
