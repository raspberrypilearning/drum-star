## Challenge

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Upgrade je project met meer drums en meer achtergronden terwijl je op meer verbazingwekkende locaties speelt. 
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

Kopieer de vorige **drum** sprite en voeg twee uiterlijken toe.

--- /task ---

--- task ---

Wijzig het `uiterlijk`{:class="block3looks"} en `geluid`{:class="block3sound"} dat wordt gebruikt in het `wanneer op deze sprite wordt geklikt`{:class="block3events"} script.

--- /task ---

--- task ---

Wijzig het aantal `slagen`{:class="block3variables"} dat wordt verdiend in het `wanneer op deze sprite wordt geklikt`{:class="block3events"} script.

--- /task ---

--- task ---

Verander het `bericht`{:class="block3events"} dat de drum laat `verschijnen`{:class="block3looks"} in een bericht voor de **nieuwe drum**.

--- /task ---

--- /collapse ---

--- collapse ---

---
title: For the 'Get' button
---

--- task ---

Kopieer de vorige **Get** sprite.

--- /task ---

--- task ---

Wijzig het `bericht`{:class="block3events"} waardoor de knop verschijnt in het `bericht`{:class="block3events"} `verzonden`{:class="block3events"} door de **vorige drum**.

--- /task ---

--- task ---

Verander het `uiterlijk`{:class="block3looks"} inclusief de kosten voor de nieuwe drum.

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

Voeg een nieuwe achtergrond toe.

--- /task ---

--- task ---

Add a script to the Stage to `switch backdrop to`{:class="block3looks"} the new backdrop when the `message`{:class="block3events"} for this drum is received.

--- /task ---

Het kan zijn dat je vindt dat je drums in een nieuwe positie moeten staan op een andere achtergrond.

--- task ---

Add a script starting with `when backdrop changes to`{:class="block3events"} to each **drum** sprite with a `go to`{:class="block3motion"} block to make them change position.

Je moet ook de beginpositie instellen `wanneer op de vlag wordt geklikt`{:class="block3events"}.

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

**Debug:** Zorg er eerst voor dat je echt begrijpt wanneer de drums en knoppen getoond moeten worden en hoe de `slagen`{:class="block3variables"} variabele moet veranderen. Het is veel gemakkelijker om een project te debuggen als je weet wat het moet doen.

--- collapse ---
---
title: My drum doesn't show/hide correctly
---

Tenzij het de eerste drum is, zou je drum een `wanneer op de vlag wordt geklikt`{:class="block3events"} script moeten hebben om `te verbergen`{:class="block3looks"}.

It should have a `when I receive`{:class="block3events"} `this drum` script to `show`{:class="block3looks"}.

Controleer of de **Get** knop voor deze drum `hetzelfde bericht uitzendt`{:class="block3events"}.

--- /collapse ---

--- collapse ---
---
title: My Get button doesn't show/hide correctly
---

Tenzij de knop voor de allereerste drum is, moet deze `verbergen`{:class="block3looks"} `wanneer op de vlag wordt geklikt`{:class="block3events"}.

It should `show`{:class="block3looks"} `when I receive`{:class="block3events"} the message for the **previous drum**.

The **Get** button should `show`{:class="block3looks"} to let the player know about the next drum they can unlock.

--- /collapse ---

--- collapse ---
---
title: I can unlock a drum when I don't have enough beats
---

Controleer of je het aantal `slagen`{:class="block3variables"} hebt gewijzigd `wanneer deze sprite op`{:class="block3events"} klikt in het script voor de **Get** knop voor de trommel.

--- /collapse ---

--- collapse ---
---
title: The number of beats doesn't change correctly when I unlock a new drum
---

Controleer of je `de beats hebt veranderd met`{:class="block3variables"} een negatief getal `wanneer op deze sprite wordt geklikt`{:class="block3events"} in het script van de **Get** knop voor de drum.

Zorg ervoor dat dit overeenkomt met het getal op het uiterlijk van de drum knop.

--- /collapse ---

--- /task ---

**Tip:** als je echt in de war raakt, is het goed om de nieuwe drum en de bijbehorende knop te verwijderen en opnieuw te beginnen. Soms is het moeilijk om een bug te vinden.

--- save ---
