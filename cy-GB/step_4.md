## Uwchraddiad cyntaf

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Byddi di'n ychwanegu dy uwchraddiad cyntaf. Bydd y botwm **Get snare** yn ymddangos ar y dechrau, fel bod y chwaraewr yn gwybod pa ddrwm mae'n gweithio tuag ato.
</div>
<div>
![](images/first-upgrade.png){:width="300px"}
</div>
</div>

--- task ---

Ychwanega'r corlun **Drum-snare** at dy brosiect a’i osod ar y Llwyfan:

![](images/snare-stage.png)

--- /task ---

--- task ---

Llusga'r sgript `pan gaiff y corlun hwn ei glicio`{:class="block3events"} o'r corlun **Drum-cymbal** i'r corlun **Drum-snare**.

[[[scratch3-copy-code]]]

--- /task ---

--- task ---

Newidia'r gwisgoedd a sain y drwm.

Newidia nifer y curiadau sy'n cael eu hennill i `2`:

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

**Profi:** Profa dy brosiect. Gwna'n yn siŵr dy fod ti'n ennill 2 guriad pan fyddi di'n clicio ar y drwm gwifrau.

--- /task ---

Dydy uwchraddiadau ddim ar gael wrth i ti ddechrau'r prosiect. Mae'n rhaid eu hennill gyda churiadau.

--- task ---

Ychwanega sgript i guddio'r corlun **drwm** yma ar ddechrau'r prosiect:

![](images/snare-icon.png)

```blocks3
when flag clicked
hide
```

--- /task ---

Bydd botwm yn dangos pa ddrwm yw'r opsiwn uwchraddio nesaf a faint o guriadau fydd yn ei gostio.

--- task ---

**Dyblyga** y corlun **Get**:

![](images/duplicate-get.png)

Newidia'r gwelededd i **Show** a newid ei enw i `Get snare`. Gosoda'r corlun yng nghornel dde isaf y Llwyfan:

![](images/get-snare.png)

--- /task ---

--- task ---

Clicia'r corlun **Drum-snare** ac wedyn mynd i'r tab **Gwisgoedd**. Defnyddia'r offeryn **Dewis** (saeth) i amlygu gwisg not hit dy ddrwm. Clicia'r eicon **Grŵp** ac wedyn yr eicon **Copïo**:

![](images/snare-icon.png)

![](images/copy-costume.png)

--- /task ---

--- task ---

Clicia dy gorlun **Get snare** a **Gludo** gwisg y drwm gwifrau. Efallai bydd angen i ti newid ei faint a'i leoli i ffitio dy fotwm:

![](images/get-snare-icon.png)

![](images/paste-costume.png)

--- /task ---

--- task ---

Clicia'r tab **Code** ac ychwanegu sgript i ddangos y corlun **Get snare** ar ddechrau’r prosiect:

![](images/get-snare-icon.png)

```blocks3
when flag clicked
show
```

--- /task ---

Dim ond os oes gan y defnyddiwr `10` curiad neu fwy y gellir prynu'r uwchraddiad. Yn [Tyfu gwas y neidr](https://projects.raspberrypi.org/en/projects/grow-a-dragonfly){:target="_blank"}, wnes di ddysgu sut i wneud penderfyniadau gyda blociau `os`{:class="block3control"}.

Mae bloc `os...yna`{:class="block3control"} yn cael ei ddefnyddio i wneud penderfyniad a bydd yn gwneud pethau gwahanol os mae amod yn `wir` neu `anwir`.

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
Rydyn ni'n defnyddio <span style="color: #0faeb0">**os ... yna**</span> drwy'r amser i wneud penderfyniadau. Pan fyddi di'n deffro, rwyt ti'n edrych i weld `os`{:class="block3control"} ydy hi'n fore. Rwyt ti'n codi, neu `fel arall`{:class="block3control"} rwyt ti'n mynd yn ôl i gysgu. Allet ti feddwl am unrhyw benderfyniadau `os ... yna`{:class="block3control"} rwyt ti'n eu gwneud? 
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
