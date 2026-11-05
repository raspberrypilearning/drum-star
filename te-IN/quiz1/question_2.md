
--- question ---

---
legend: Question 2 of 3
---

ఒక ప్రాజెక్ట్, యూజర్ యొక్క పేరు అడగడం `ask`{:class="block3sensing"} కోసం ఈ స్క్రిప్ట్‌ను కలిగి ఉంది:

```blocks3
when flag clicked
set [name v] to [???] 
ask [What's your name?] and wait 
set [name v] to (answer)
```

![](images/q1-chatbot.png)

ప్లేయర్ టిక్ (చెక్‌మార్క్)పై క్లిక్ చేసి, స్క్రిప్ట్ పూర్తయిన తర్వాత `name`{:class="block3variables"} వేరియబుల్ విలువ ఎంత అవుతుంది?

--- choices ---

- ( )  name

  --- feedback ---

లేదు, `name`{:class="block3variables"} అనేది వేరియబుల్‌ పేరు.

  --- /feedback ---

- ( ) ???

  --- feedback ---

లేదు, `???` అనేది, `ask`{:class="block3sensing"} బ్లాక్ అమలు కావడానికి ముందు `name`{:class="block3variables"} వేరియబుల్ యొక్క విలువ.

  --- /feedback ---

- ( ) answer

  --- feedback ---

లేదు, `answer`{: class = "block3sensing"} అనేదె Scratch లో గల బిల్ట్ ఇన్ వేరియబుల్, అది `ask`{:class = "block3sensing"} ప్రశ్న అడిగినపుడు, యూజర్ టైప్ చేసిన సమాధానం నిల్వ చేయడానికి ఉపయోగించ బడుతుంది. --- /feedback ---

- (x) Bobo

  --- feedback ---

అవును, `set [name v] to`{:class="block3variables"} బ్లాక్ `name`{:class="block3variables"} వేరియబుల్ యొక్క **విలువ** ను, యూజర్ నమోదు చేసిన టెక్స్ట్ ని `answer`{:class="block3sensing"} గా ఇది సెట్ చేస్తుంది.

`Bobo` విలువ కూడా Stage పై చూపబడుతుంది.

  --- /feedback ---

--- /choices ---

--- /question ---
