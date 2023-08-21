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
+change [beats v] by [2] //2 beats per click
+switch costume to [drum-snare-b v] //hit costume
+play drum [(1) Snare Drum v] for [0.25] beats //drum sound
+switch costume to [drum-snare-a v] //not hit costume
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

విజిబిలిటీని **Show**కి మార్చండి మరియు దాని పేరును `Get snare`కి మార్చండి. Stage యొక్క దిగువ-కుడి మూలలో దాన్ని ఉంచండి:

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

`10` లేదా అంతకంటే ఎక్కువ బీట్‌లను కలిగి ఉంటే మాత్రమే అప్‌గ్రేడ్ కొనుగోలు చేయబడుతుంది. [Grow a dragonfly](https://projects.raspberrypi.org/en/projects/grow-a-dragonfly){:target="_blank"}లో, మీరు `if`{:class="block3control"} బ్లాక్‌లతో నిర్ణయాలు తీసుకోవడం గురించి తెలుసుకున్నారు.

`if ... else`{:class="block3control"} బ్లాక్ నిర్ణయం తీసుకోవడానికి ఉపయోగించబడుతుంది మరియు కండిషన్ `true` లేదా `false`అయితే తదనుగుణంగా వివిధ పనులను చేస్తుంది.

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
మనము నిర్ణయాలు తీసుకొనే అన్ని సమయాలలో <span style="color: #0faeb0">**if ... else**</span> ను ఉపయోగిస్తాము. మీరు మేల్కొన్నప్పుడు, మీరు `if`{:class="block3control"} ఇది ఉదయమా అని తనిఖీ చేస్తారు. మీరు లేస్తారు `else`{:class="block3control"} మీరు తిరిగి నిద్రపోతారు. మీరు తీసుకొనే ఏదైనా `if ... else`{:class="block3control"} నిర్ణయాల గురించి ఆలోచించగలరా? 
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
