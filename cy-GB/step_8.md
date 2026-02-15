## Challenge

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Galli di uwchraddio dy brosiect gyda rhagor o ddrymiau a mwy o gefnlenni wrth i ti chwarae mewn mwy o leoliadau anhygoel. 
</div>
<div>
![](images/upgrade-project.png){:width="300px"}
</div>
</div>

### Add more drums

To add another drum to unlock, look back at the earlier steps of the project.

Here are some reminders if you need them.

--- collapse ---

---
title: For the drum
---

--- task ---

Ddyblygu'r corlun **drum** blaenorol ac ychwanegu dwy wisg.

--- /task ---

--- task ---

Newid y `wisg`{:class="block3looks"} a'r `sain`{:class="block3sound"} sy'n cael eu defnyddio yn y sgript `pan gaiff y corlun hwn ei glicio`{:class="block3events"}.

--- /task ---

--- task ---

Newid nifer y `curiadau`{:class="block3variables"} sy'n cael eu hennill yn y sgript `pan gaiff y corlun hwn ei glicio`{:class="block3events"}.

--- /task ---

--- task ---

Newid y `neges`{:class="block3events"} sy'n gwneud i'r drwm `ddangos`{:class="block3looks"} i neges ar gyfer y **drwm newydd**.

--- /task ---

--- /collapse ---

--- collapse ---

---
title: For the 'Get' button
---

--- task ---

Dyblyga'r corlun **Get** blaenorol.

--- /task ---

--- task ---

Newidia'r `neges`{:class="block3events"} sy'n gwneud i'r botwm ymddangos i'r `neges`{:class="block3events"} sy'n cael ei `darlledu`{:class="block3events"} gan y **drwm blaenorol**.

--- /task ---

--- task ---

Newidia'r `wisg`{:class="block3looks"} gan gynnwys cost y drwm newydd.

--- /task ---

--- task ---

Change the number of `beats`{:class="block3variables"} you must have to unlock this drum in the `if`{:class="block3events"} condition. Change the negative number of `beats`{:class="block3variables"} you `change by`{:class="block3variables"} when you unlock this drum. Change the number that `beats`{:class="block3variables"} needs to be subtracted from in the `join`{:class="block3operators"} block. Change the message that is `broadcast`{:class="block3events"} to the name of the **new drum**.

--- /task ---

--- /collapse ---

--- collapse ---

---
title: For the venue
---

--- task ---

Ychwanegu cefnlen newydd.

--- /task ---

--- task ---

Add a script to the Stage to `switch backdrop to`{:class="block3looks"} the new backdrop when the `message`{:class="block3events"} for this drum is received.

--- /task ---

Efallai y gweli fod angen i dy ddrymiau fod mewn safle newydd ar gefnlen wahanol.

--- task ---

Add a script starting with `when backdrop changes to`{:class="block3events"} to each **drum** sprite with a `go to`{:class="block3motion"} block to make them change position.

Bydd hefyd angen i ti osod eu safleoedd cychwynnol `ar ôl clicio'r faner`{:class="block3events"}.

--- /task ---

--- /collapse ---

### Improve feedback to the player

Tell the player exactly **how many more** beats are needed to unlock the next drum.

--- task ---

Add this code to `join`{:class="block3operators"} the number of beats needed with the text you have used to tell the player they need more beats if they do not have enough to unlock the next drum:

```blocks3
when this sprite clicked
if <(beats)>  [9]> then //if 10 or more beats
hide
change [beats v] by [-10] //take away the cost of upgrade
else
+ say (join ((10) - (beats)) [beats needed!]) for [2] seconds
end
```

**Note**: Update the numbers to match those needed to unlock each drum.

--- /task ---

### Tidy your code

--- task ---

**Tidy:** If you have time, then it's a good idea to make sure the sprites in the sprite list are in a sensible order, starting with the drums in their locked order and then the buttons in order.

--- /task ---

--- task ---

### Stuck?

**Debug:** Yn gyntaf gwna'n siŵr dy fod yn deall yn iawn pryd y dylai'r drymiau a'r botymau ymddangos a sut y dylai'r newidyn `curiadau`{:class="block3variables"} newid. Mae'n llawer haws difa chwilod prosiect os wyt ti'n glir am yr hyn mae i fod i'w wneud.

--- collapse ---
---
title: My drum doesn't show/hide correctly
---

Oni bai mai hwn ydy'r drwm cyntaf, dylai dy ddrwm gael sgript `pan fydd y faner wedi'i chlicio`{:class="block3events"} i'w `guddio`{:class="block3looks"}.

It should have a `when I receive`{:class="block3events"} `this drum` script to `show`{:class="block3looks"}.

Gwiria fod y botwm **Get** ar gyfer y drwm yma yn `darlledu`{:class="block3events"} yr un neges.

--- /collapse ---

--- collapse ---
---
title: My Get button doesn't show/hide correctly
---

Oni bai fod y botwm ar gyfer y drwm cyntaf un, dylai `guddio`{:class="block3looks"} `pan fydd y faner wedi'i chlicio`{:class="block3events"}.

It should `show`{:class="block3looks"} `when I receive`{:class="block3events"} the message for the **previous drum**.

The **Get** button should `show`{:class="block3looks"} to let the player know about the next drum they can unlock.

--- /collapse ---

--- collapse ---
---
title: I can unlock a drum when I don't have enough beats
---

Gwna'n siŵr dy fod wedi newid nifer y `curiadau`{:class="block3variables"} sydd eu hangen `pan gaiff y corlun hwn ei glicio`{:class="block3events"} yn y sgript ar gyfer y botwm **Get** ar gyfer y drwm.

--- /collapse ---

--- collapse ---
---
title: The number of beats doesn't change correctly when I unlock a new drum
---

Gwna'n siŵr dy fod wedi `newid curiadau gan`{:class="block3variables"} gyda rhif negatif `pan gaiff y corlun hwn ei glicio`{:class="block3events"} yn y sgript ar gyfer y botwm **Get** ar gyfer y drwm.

Sicrha fod hyn yn cyfateb i rif gwisg botwm y drwm.

--- /collapse ---

--- /task ---

**Awgrym:** Os wyt ti'n dechrau drysu, mae'n iawn dileu'r drwm newydd a'i fotwm, a dechrau eto. Weithiau mae'n anodd dod o hyd i chwilod.

--- save ---
