## మొదటి అప్‌గ్రేడ్

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
మీరు మీ మొదటి అప్‌గ్రేడ్‌ని జోడిస్తారు. **Get snare** బటన్ ప్రారంభంలో చూపబడుతుంది, తద్వారా వారు ఏ డ్రమ్ వైపు పని చేస్తున్నారో ప్లేయర్‌కు తెలుస్తుంది.
</div>
<div>
![](images/first-upgrade.png){:width="300px"}
</div>
</div>

--- task ---

**Drum-snare** sprite మీ ప్రాజెక్ట్ కు జోడించి, Stage పై ఉంచండి:

![](images/snare-stage.png)

--- /task ---

--- task ---

`when this sprite clicked`{:class="block3events"} స్క్రిప్ట్‌ను **Drum-cymbal** sprite నుండి **Drum-snare** sprite కి డ్రాగ్ చేయండి.

[[[scratch3-copy-code]]]

--- /task ---

--- task ---

Costume మరియు డ్రమ్ సౌండ్ మార్చండి.

సంపాదించిన బీట్‌ల సంఖ్యను `2`కి మార్చండి:

![](images/snare-icon.png)

```blocks3
when this sprite clicked
+change [beats v] by [2] //ప్రతి క్లిక్‌కి 2 బీట్‌లు
+switch costume to [drum-snare-b v] //హిట్ costume
+play drum [(1) Snare Drum v] for [0.25] beats //డ్రమ్ ధ్వని
+switch costume to [drum-snare-a v] //హిట్ costume కాదు
```

--- /task ---

--- task ---

**పరీక్ష:** మీ ప్రాజెక్ట్‌ని ప్రయత్నించండి. మీరు snare డ్రమ్‌పై క్లిక్ చేసినప్పుడు మీరు 2 బీట్‌లను సంపాదించారని నిర్ధారించుకోండి.

--- /task ---

మీరు ప్రాజెక్ట్‌ను ప్రారంభించినప్పుడు అప్‌గ్రేడ్‌లు అందుబాటులో లేవు. వాటిని బీట్లతో సంపాదించుకోవాలి.

--- task ---

ప్రాజెక్ట్ ప్రారంభంలో **drum** spriteను దాచడానికి స్క్రిప్ట్‌ను జోడించండి:

![](images/snare-icon.png)

```blocks3
when flag clicked
hide
```

--- /task ---

ఒక బటన్ తదుపరి అప్‌గ్రేడ్ ఎంపిక ఏ డ్రమ్ మరియు దానికి ఎన్ని బీట్‌లు ఖర్చవుతాయి అని చూపుతుంది.

--- task ---

**Get** sprite ని **Duplicate** చేయండి:

![](images/duplicate-get.png)

విజిబిలిటీని **Show**కి మార్చండి మరియు దాని పేరును `Get snare` కి మార్చండి. Stage యొక్క దిగువ-కుడి మూలలో దాన్ని ఉంచండి:

![](images/get-snare.png)

--- /task ---

--- task ---

**Drum-snare** sprite పై క్లిక్ చేసి, **Costumes** ట్యాబ్‌కి వెళ్లండి. మీ డ్రమ్ యొక్క నాట్ హిట్ costume ని హైలైట్ చేయడానికి **Select** (బాణం) సాధనాన్ని ఉపయోగించండి. **Group** చిహ్నంపై క్లిక్ చేసి, ఆ తరువాత **Copy** చిహ్నంపై క్లిక్ చేయండి:

![](images/snare-icon.png)

![](images/copy-costume.png)

--- /task ---

--- task ---

మీ **Get snare** sprite మరియు **Paste** snare costume పై క్లిక్ చేయండి. మీరు మీ బటన్‌కు సరిపోయేలా పరిమాణాన్ని మార్చడం మరియు పొజిషన్ లో ఉంచడం అవసరం కావచ్చు:

![](images/get-snare-icon.png)

![](images/paste-costume.png)

--- /task ---

--- task ---

**Code** ట్యాబ్‌పై క్లిక్ చేసి, ప్రాజెక్ట్ ప్రారంభంలో **Get snare** sprite ను చూపించడానికి స్క్రిప్ట్‌ను జోడించండి:

![](images/get-snare-icon.png)

```blocks3
when flag clicked
show
```

--- /task ---

`10` లేదా అంతకంటే ఎక్కువ బీట్‌లను కలిగి ఉంటే మాత్రమే అప్‌గ్రేడ్ కొనుగోలు చేయబడుతుంది. [Grow a dragonfly](https://projects.raspberrypi.org/te-IN/projects/grow-a-dragonfly){:target="_blank"} లో, మీరు `if`{:class="block3control"} బ్లాక్‌లతో నిర్ణయాలు తీసుకోవడం గురించి తెలుసుకున్నారు.

`if ... else`{:class="block3control"} బ్లాక్ నిర్ణయం తీసుకోవడానికి ఉపయోగించబడుతుంది మరియు కండిషన్ `true` లేదా `false` అయితే తదనుగుణంగా వివిధ పనులను చేస్తుంది.

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
మనము నిర్ణయాలు తీసుకొనే అన్ని సమయాలలో <span style="color: #0faeb0">**if ... else**</span> ను ఉపయోగిస్తాము. మీరు మేల్కొన్నప్పుడు, మీరు `if`{:class="block3control"} ఇది ఉదయమా అని తనిఖీ చేస్తారు. మీరు లేస్తారు `else`{:class="block3control"} మీరు తిరిగి నిద్రపోతారు. మీరు తీసుకొనే ఏదైనా `if ... else`{:class="block3control"} నిర్ణయాల గురించి ఆలోచించగలరా? 
</p>

--- task ---

`if`{:class="block3control"} ప్లేయర్‌కు తగినంత బీట్‌లు ఉంటే, అప్‌గ్రేడ్ చేయడానికి ఈ కోడ్‌ను జోడించండి లేదా వారు అప్‌గ్రేడ్ చేయలేకపోతే `Not enough beats!` అని `say`{:class="block3looks"} తో చెప్పండి:

![](images/get-snare-icon.png)

```blocks3
when this sprite clicked
if <(beats)>  [9]> then //10 లేదా అంతకంటే ఎక్కువ బీట్స్ ఉంటే
hide
change [beats v] by [-10] //కాస్ట్ అప్‌గ్రేడ్‌ను తీసివేయండి
else
say [Not enough beats!] for [2] seconds 
end
```

--- /task ---

Snare అప్‌గ్రేడ్ కొనుగోలు చేయబడిందని ఇతర sprite లు మరియు Stage కి తెలియజేయండి.

--- task ---

`snare` సందేశాన్ని `broadcast`{:class="block3events"} చేయడానికి బ్లాక్‌ను జోడించండి:

![](images/get-snare-icon.png)

```blocks3
when this sprite clicked
if <(beats)>  [9]> then // 10 లేదా అంతకంటే ఎక్కువ బీట్స్ ఉంటే
hide
change [beats v] by [-10] // కాస్ట్ అప్‌గ్రేడ్‌ను తీసివేయండి
+ broadcast (snare v) // మీ డ్రమ్ పేరు
else
say [Not enough beats!] for [2] seconds 
end
```

--- /task ---

--- task ---

**Drum-snare** sprite పై క్లిక్ చేయండి. ఈ స్క్రిప్ట్‌ని జోడించండి:

![](images/snare-icon.png)

```blocks3
when I receive [snare v]
show
```

--- /task ---

మీరు మీ పరికరాలను అప్‌గ్రేడ్ చేసినప్పుడు, మీరు పెద్ద వేదికలలో ప్లే చేయగలరు.

--- task ---

మరొక బ్యాక్‌డ్రాప్‌ను జోడించండి. మనము పాఠశాలలో మన రెండవ ప్రదర్శనను ప్లే చేయడానికి **Chalkboard** ను ఎన్నుకొందాము.

అప్‌గ్రేడ్ సందేశాన్ని స్వీకరించినప్పుడు `switch backdrop`{:class="block3looks"} మార్చడానికి Stage కి కోడ్‌ని జోడించండి:

![](images/stage-icon.png)

```blocks3
when I receive [snare v]
switch backdrop to [Chalkboard v]
```

**చిట్కా:** బెడ్ రూమ్ నుండి ఒక చిన్న మెట్టు పైకి ఉండే వేదికను ఎంచుకోండి. మీరు ముందు కాలం కోసం పెద్ద వేదికలను సేవ్ చేయాలనుకుంటున్నారు.

--- /task ---

--- task ---

**పరీక్ష:** మీ ప్రాజెక్ట్‌ను అమలు చేయండి. మీరు తగినంత బీట్‌లను కలిగి ఉండటానికి ముందు స్నేర్ అప్‌గ్రేడ్‌ను ప్రయత్నించండి మరియు కొనుగోలు చేయండి.

మీరు అప్‌గ్రేడ్ చెక్‌ను కొనుగోలు చేసినప్పుడు: snare కనిపిస్తుంది, బటన్ అదృశ్యమవుతుంది, వేదిక మారుతుంది మరియు `beats`{:class="block3variables"} `10` వరకు తగ్గుతాయి.

--- /task ---

--- save ---
