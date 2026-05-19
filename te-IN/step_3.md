## స్టార్టర్ డ్రమ్

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
మీరు బీట్‌లను సంపాదించడానికి మరియు సౌండ్ ప్లే చేయడానికి క్లిక్ చేయగల **cymbal** spriteని జోడిస్తారు.
</div>
<div>
![](images/starter-drum.png){:width="300px"}
</div>
</div>

--- task ---

Click **Choose a Sprite** and search `cymbal`.

![](images/cymbal-gallery.png)

--- /task ---

--- task ---

Add the **Drum-cymbal** sprite and position it on the Stage:

![](images/cymbal-stage.png)

--- /task ---

--- task ---

**Music extension** ని జోడించండి:

[[[generic-scratch3-add-music-extension]]]

--- /task ---

--- task ---

Cymbal `switch costume`{:class="block3looks"} చేయడానికి, ఇంకా `play a drum sound`{:class="block3extensions"} స్క్రిప్ట్‌ను జోడించండి:

![](images/cymbal-icon.png)

```blocks3
ఈ స్ప్రైట్ ని క్లిక్ చేసినప్పుడు
స్విచ్ కాస్ట్యూమ్‌ టు [drum-cymbal-b v]  // hit costume
ప్లే డ్రమ్ [(5) Open High-Hat v] [0.25] బీట్‌ల కోసం // drum sound
స్విచ్ కాస్ట్యూమ్‌ టు [drum-cymbal-a v] కి మార్చండి // not hit costume
```

--- /task ---

--- task ---

**పరీక్ష:** మీ cymbal పై క్లిక్ చేయడం ద్వారా పరీక్షించండి.

You should hear a sound and see the costume change.

--- /task ---

**Drum-cymbal** sprite మీరు క్లిక్ చేసిన ప్రతిసారీ మీకు ఒక బీట్‌ని సంపాదిస్తుంది.

--- task ---

Create a `variable`{:class="block3variables"} (for all sprites) called `beats`:

![](images/beats-variable.png)

--- /task ---

--- task ---

**Drum-cymbal** sprite పై క్లిక్ చేసినప్పుడు `change beats by`{:class="block3variables"} కు ఒక బ్లాక్‌ను జోడించండి:

```blocks3
when this sprite clicked
+change [beats v] by [1]
switch costume to [drum-cymbal-b v]
play drum [(5) Open High-Hat v] for [0.25] beats 
switch costume to [drum-cymbal-a v]
```

--- /task ---

--- task ---

**Test:** Test the **Drum-cymbal** by clicking on it.

You should see the `beats`{:class="block3variables"} increase.

--- /task ---

మీరు కొత్త గేమ్‌ని ప్రారంభించినప్పుడు `beats`{:class="block3variables"} వేరియబుల్ `0` బీట్‌ల వద్ద ప్రారంభం కావాలి.

--- task ---

Click on the Stage pane and then the **Code** tab.

`set beats to`{:class="block3variables"} `0` కి బ్లాక్‌ని జోడించండి:

![](images/stage-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) 
set [name v] to [???] 
+ set [beats v] to [0]
```
--- /task ---

--- task ---

**పరీక్ష:** ఆకుపచ్చ జెండాను క్లిక్ చేయండి మరియు మీ `beats`{:class="block3variables"} వేరియబుల్ `0`వద్ద ప్రారంభమవుతుందని నిర్ధారించుకోండి.

--- /task ---

--- save ---
