
--- question ---

---
legend: 3లో 3వ ప్రశ్న
---

ప్లేయర్ వారి డ్రమ్‌ని అప్‌గ్రేడ్ చేయడానికి బటన్‌పై క్లిక్ చేసినప్పుడు ఏమి జరుగుతుందో నియంత్రించడానికి మీరు ఈ స్క్రిప్ట్‌ని ఉపయోగించారు:

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

`beats`{:class="block3variables"} వేరియబుల్ విలువ `29`, ప్లేయర్ బటన్‌పై క్లిక్ చేసినప్పుడు ఏమి జరుగుతుంది?

--- choices ---

- ( ) sprite `hide` {:class="block3looks"} అవుతుంది

  --- feedback ---

  పూర్తిగా నిజం కాదు `hide`{:class="block3looks"} బ్లాక్ ఉంది, కానీ అది `29` `beats`{:class="block3variables"}తో రన్ చేయబడదు. స్క్రిప్ట్‌ని మళ్లీ ఒకసారి చూడండి.

  --- /feedback ---

- (x) బటన్ sprite `say`{:class="block3looks"} `Not enough beats!`

  --- feedback ---

అపును, `beats`{:class="block3variables"} విలువ `29`కంటే ఎక్కువగా ఉందో లేదో కండిషన్ తనిఖీ చేస్తుంది, అయితే `beats`{:class="block3variables"} `29` కి సమానం కాబట్టి ప్లేయర్‌కు తగినంత బీట్స్ లేవు.

  --- /feedback ---

- ( ) `beats`{:class="block3variables"} వేరియబుల్ విలువ నుండి 30 తీసివేయబడుతుంది

  --- feedback ---

  లేదు, `beats`{:class="block3variables"} వేరియబుల్ విలువ అలాగే ఉంటుంది. `beats`{:class="block3variables"} విలువ `29` అంటే `beats`{:class="block3variables"} `> 29` తప్పు, కాబట్టి ` if `{:class ="block3control"} బ్లాక్ అమలు చేయబడదు.

  --- /feedback ---

- ( ) ఏమిలేదు

  --- feedback ---

  లేదు, స్క్రిప్ట్ ఎప్పుడూ ఏదో ఒకటి చేస్తుంది. `29` `beats`{:class="block3variables"} ఉన్నప్పుడు స్క్రిప్ట్‌లోని ఏ భాగం రన్ అవుతుందో చూడటానికి నిశితంగా పరిశీలించండి.

  --- /feedback ---

--- /choices ---

--- /question ---
