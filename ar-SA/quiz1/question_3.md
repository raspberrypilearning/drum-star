
--- question ---

---
legend: السؤال 3 من 3
---

لقد استخدمت هذا المقطع البرمجي للتحكم في ما يحدث عندما ينقر اللاعب على الزر لترقية الطبلة الخاصة به:

```blocks3
when this sprite clicked
if <(دقة)>  [29]> then 
hide
change [دقة v] by [-30] 
broadcast [conga v] 
else
say [عدد غير كافي من الدقات] for [2] seconds 
end
```

إذا كانت قيمة `النبضات`{:class="block3variables"} هو `29`، ماذا سيحدث عندما ينقر اللاعب على الزر؟

--- choices ---

- ( ) الكائن سوف `يختفي `{:class="block3looks"}

--- feedback ---

ليس تمامًا ، هناك لبنة `إخفاء`{:class="block3looks"} في المقطع البرمجي ، لكنها لن تعمل مع`29``ضربات`{:class="block3variables"}. ألق نظرة على المقطع البرمجي مرة أخرى.

  --- /feedback ---

- (x) نكائن الزر `سيقول`{:class="block3looks"} `عدد غير كافي من الدقات`

  --- feedback ---

نعم ، يتحقق الشرط مما إذا كانت `نبضة`{:class="block3variables"} أكبر من `29`، لكن `ضربات`{:class="block3variables"} تساوي `29` لذلك لا يملك اللاعب ما يكفي.

  --- /feedback ---

- ( ) سيتم أخذ 30 من قيمة متغيير `نبضة`{:class="block3variables"}

  --- feedback ---

  لا ، قيمة المتغير `نبضة`{:class="block3variables"} ستبقى كما هي. `نبضة`{:class="block3variables"} هي `29` مما يعني أن `ضربات`{:class="block3variables"} `> 29` خاطئة ، لذا فإن اللبنة في الجزء الأول من `اذا`{:class="block3control"}.

  --- /feedback ---

- ( ) لا شئ

  --- feedback ---

  لا ، هذا المقطع البرمجي سيفعل شيئًا دائمًا. ألق نظرة فاحصة لمعرفة أي جزء من المقطع البرمجي سيتم تشغيله عندما يكون لديك `29` `نبضات`{:class="block3variables"}.

  --- /feedback ---

--- /choices ---

--- /question ---
