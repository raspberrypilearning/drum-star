## Drwm cychwynnol

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Byddi di'n ychwanegu corlun **symbal** y galli di ei glicio i ennill curiadau a chwarae sain.
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

Ychwanega'r **Estyniad sain**:

[[[generic-scratch3-add-music-extension]]]

--- /task ---

--- task ---

Ychwanega sgript i wneud i'r symbal `newid gwisg`{:class="block3looks"} a `chwarae sain drwm`{:class="block3extensions"}:

![](images/cymbal-icon.png)

```blocks3
when this sprite clicked
switch costume to [drum-cymbal-b v] // hit costume
play drum [(5) Open High-Hat v] for [0.25] beats // drum sound
switch costume to [drum-cymbal-a v]  // not hit costume
```

--- /task ---

--- task ---

**Prawf:** Profa dy cymbal trwy glicio arno.

You should hear a sound and see the costume change.

--- /task ---

Bydd y corlun **Drum-cymbal** yn ennill un curiad i ti bob tro byddi di'n ei glicio.

--- task ---

Create a `variable`{:class="block3variables"} (for all sprites) called `beats`:

![](images/beats-variable.png)

--- /task ---

--- task ---

Ychwanega floc er mwyn `newid curiadau gan 1`{:class="block3variables"} pan gaiff y corlun **Drum-cymbal** ei glicio:

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

Mae angen i'r newidyn `curiadau`{:class="block3variables"} ddechrau ar `0` curiad pan fyddi di'n dechrau gêm newydd.

--- task ---

Click on the Stage pane and then the **Code** tab.

Ychwanega floc er mwyn `gosod curiadau i`{:class="block3variables"} `0`:

![](images/stage-icon.png)

```blocks3
when flag clicked
switch backdrop to (Bedroom 3 v) 
set [name v] to [???] 
+ set [beats v] to [0]
```
--- /task ---

--- task ---

**Prawf:** Clicia'r faner werdd a gwneud yn siŵr bod dy newidyn `curiadau`{:class="block3variables"} yn dechrau ar `0`.

--- /task ---

--- save ---
