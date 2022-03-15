## మీ ప్రాజెక్ట్‌ను అప్‌గ్రేడ్ చేయండి

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
మీరు మరిన్ని అద్భుతమైన వేదికలపై ప్లే చేస్తున్నప్పుడు మరిన్ని డ్రమ్స్ మరియు మరిన్ని బ్యాక్‌డ్రాప్‌లతో మీ ప్రాజెక్ట్‌ను అప్‌గ్రేడ్ చేయండి. 
</div>
<div>
![](images/upgrade-project.png){:width="300px"}
</div>
</div>

మీ ప్రాజెక్ట్‌కు మరిన్ని అప్‌గ్రేడ్‌లను జోడించడానికి ఎంచుకోవడానికి చాలా ఎక్కువ డ్రమ్ costume లు ఉన్నాయి.

అప్‌గ్రేడ్ చేయడానికి మరొక డ్రమ్‌ని జోడించడానికి, ప్రాజెక్ట్ యొక్క మునుపటి దశలను తిరిగి చూడండి.

**drum**, కోసం మీరు వీటిని చేయాలి:

--- task ---

**drum** sprite ని నకలు చేసి, రెండు costume లను జోడించండి.

--- /task ---

--- task ---

`when this sprite clicked`{:class="block3events"} స్క్రిప్ట్ లో ఉపయోగించిన `costume`{:class="block3looks"} మరియు `sound`{:class="block3sound"} ని మార్చండి.

--- /task ---

--- task ---

`when this sprite clicked`{:class="block3events"} స్క్రిప్ట్ లో సాధించిన `beats`{:class="block3variables"} సంఖ్యని మార్చండి.

--- /task ---

--- task ---

**new drum** సందేశానికి బదులుగా, డ్రమ్‌ని `show`{:class="block3looks"} చేసే `message`{:class="block3events"} ని మార్చండి.

--- /task ---

**button**, కోసం మీరు వీటిని చేయాలి:

--- task ---

**Get** sprite ను నకలు చేయండి.

--- /task ---

--- task ---

**మునుపటి డ్రమ్** యొక్క`broadcast`{:class="block3events"} `message`{:class="block3events"} కి అనుగుణంగా బటన్ ను కనిపింపజేసే `message`{:class="block3events"} ను మార్పు చేయండి.

--- /task ---

--- task ---

కొత్త డ్రమ్ వెలతో సహా `costume`{:class="block3looks"}ని మార్చండి.

--- /task ---

--- task ---

మీరు ఈ డ్రమ్‌ను `if`{:class="block3events"} కండిషన్‌లో పొందడానికి తప్పనిసరిగా కావల్సిన `beats`{:class="block3variables"} సంఖ్యను మార్చండి,. `change by`{:class="block3variables"} ద్వారా మీరు ఈ డ్రమ్‌ని పొందినప్పుడు కల `beats`{:class="block3variables"} యొక్క నెగటివ్ సంఖ్యను మార్చండి. **కొత్త డ్రమ్** పేరుకు `broadcast`{:class="block3events"} అయ్యే సందేశాన్ని మార్చండి.

--- /task ---

**వేదిక**, కోసం మీరు వీటిని చేయాలి:

--- task ---

కొత్త బ్యాక్‌డ్రాప్‌ని జోడించండి.

--- /task ---

--- task ---

ఈ డ్రమ్ కోసం `message`{:class="block3events"} పొందినపుడు, `switch backdrop to`{:class="block3looks"} ద్వారా కొత్త బ్యాక్‌డ్రాప్‌ కోసం Stage కు స్క్రిప్ట్ ను జోడించండి.

--- /task ---

మీ డ్రమ్స్ వేరే బ్యాక్‌డ్రాప్‌లో కొత్త స్థానంలో ఉండాలని మీరు కనుగొనవచ్చు.

--- task ---

ప్రతి **drum** sprite కు `when backdrop changes to`{:class="block3events"} తో మొదలయ్యే స్క్రిప్ట్ ను జోడించండి మరియు పొజిషన్ మార్చడానికి `go to`{:class="block3motion"} బ్లాక్ ను కూడా.

మీరు `when flag clicked `{:class="block3events"} క్లిక్ చేసినప్పుడు వాటి ప్రారంభ స్థానాన్ని కూడా సెట్ చేయాలి.

--- /task ---

--- task ---

**క్రమ పద్ధతిగా:** మీకు సమయం ఉంటే, sprite జాబితాలోని sprite లు వాటి అప్‌గ్రేడ్ క్రమంలో డ్రమ్‌లతో ప్రారంభించి, ఆపై బటన్‌లను క్రమంలో ఉండేలా చూసుకోవడం మంచిది.

--- /task ---

--- task ---

**డీబగ్:** ముందుగా డ్రమ్‌లు మరియు బటన్‌లు ఎప్పుడు చూపాలి మరియు `beats`{:class="block3variables"} వేరియబుల్ ఎలా మారాలి అని మీరు నిజంగా అర్థం చేసుకున్నారని నిర్ధారించుకోండి. ప్రాజెక్ట్ ఏమి చేయాలో మీకు స్పష్టంగా ఉంటే దాన్ని డీబగ్ చేయడం చాలా సులభం.

--- collapse ---
---
title: నా డ్రమ్ సరిగ్గా చూపడం/దాగడం లేదు
---

అది మొదటి డ్రమ్ అయితే తప్ప, `when flag clicked`{:class="block3events"} `hide`{:class="block3looks"} చేయడానికి మీ డ్రమ్ ఒక స్క్రిప్ట్ ను కలిగి ఉండాలి. మరియు అది `when I receive`{:class="block3events"} `this drum` `show`{:class="block3looks"} స్క్రిప్ట్‌ని కలిగి ఉండాలి.

ఈ డ్రమ్ కోసం **Get** బటన్ అదే సందేశాన్ని `broadcast`{:class="block3events"} చేసేలా తనిఖీ చేయండి.


--- /collapse ---

--- collapse ---
---
title: నా డ్రమ్ సరిగ్గా చూపడం/దాగడం లేదు
---

బటన్ మొదటి డ్రమ్ కోసం తప్ప,`when flag clicked`{:class="block3events"} అది `hide`{:class="block3looks"} చేయాలి. మరియు `when I receive`{:class="block3events"} సందేశం **మునుపటి డ్రమ్** కోసం అందినప్పుడు `show`{:class="block looks"} అవబడాలి. **Get** బటన్ `show`{:class="block3looks"} అవడం ద్వారా, ప్లేయర్‌కు వారు పని చేస్తున్న తదుపరి అప్‌గ్రేడ్ గురించి తెలియజేయాలి.

--- /collapse ---

--- collapse ---
---
title: నా దగ్గర తగినంత బీట్స్ లేనప్పుడు నేను డ్రమ్ కొనగలను
---

డ్రమ్ యొక్క **Get** బటన్ కోసం స్క్రిప్ట్ లో `when this sprite clicked`{:class="block3events"} కోసం అవసరమయిన `beats`{:class="block3variables"} సంఖ్యని మీరు మార్పు చేసేలా తనిఖీ చేసుకోండి.

--- /collapse ---

--- collapse ---
---
title: నేను కొత్త డ్రమ్‌ని పొందినప్పుడు బీట్‌ల సంఖ్య సరిగ్గా మారదు
---

డ్రమ్ యొక్క **Get** బటన్ కోసం స్క్రిప్ట్ లో `when this sprite clicked`{:class="block3events"} కోసం `changed beats by`{:class="block3variables"} నెగటివ్ సంఖ్య అయ్యేలా మీరు తనిఖీ చేసుకోండి.

ఇది డ్రమ్ బటన్ cistume లోని నంబర్‌తో సరిపోలుతుందని నిర్ధారించుకోండి.

--- /collapse ---

--- /task ---

--- collapse ---
---
title: పూర్తయిన ప్రాజెక్ట్
---

మీరు [పూర్తయిన ప్రాజెక్ట్‌ను ఇక్కడ](https://scratch.mit.edu/projects/660066022/){:target="_blank"} వీక్షించవచ్చు.

--- /collapse ---

**చిట్కా:** మీరు నిజంగా గందరగోళానికి గురైతే, కొత్త డ్రమ్ మరియు దాని బటన్‌ను తొలగించి, మళ్లీ ప్రారంభించడం మంచిది. కొన్నిసార్లు బగ్‌ని గుర్తించడం కష్టం.

--- save ---
