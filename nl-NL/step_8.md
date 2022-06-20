## Verbeter je project

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Upgrade je project met meer drums en meer achtergronden terwijl je op meer verbazingwekkende locaties speelt. 
</div>
<div>
![](images/upgrade-project.png){:width="300px"}
</div>
</div>

Er zijn veel meer drum uiterlijken om uit te kiezen om meer upgrades aan je project toe te voegen.

Als je nog een drum wilt toevoegen om naar te upgraden, kijk dan terug naar de eerdere stappen van het project.

Voor de **drum** moet je:

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

Voor de **knop** moet je:

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

Verander het aantal `slagen`{:class="block3variables"} dat je moet hebben om deze drum te krijgen in de `als`{:class="block3events"} conditie. Verander het negatieve aantal `slagen`{:class="block3variables"} je `verandert met`{:class="block3variables"} wanneer je deze drum krijgt. Wijzig het bericht dat het`zend signaal`{:class="block3events"} blok krijgt in de naam van de **nieuwe drum**.

--- /task ---

Voor de **locatie** moet je:

--- task ---

Voeg een nieuwe achtergrond toe.

--- /task ---

--- task ---

Voeg een script toe aan het speelveld om `achtergrond te veranderen in`{:class="block3looks"} de nieuwe achtergrond wanneer het `bericht`{:class="block3events"} voor deze drum wordt ontvangen.

--- /task ---

Het kan zijn dat je vindt dat je drums in een nieuwe positie moeten staan op een andere achtergrond.

--- task ---

Voeg een script toe dat begint met `wanneer de achtergrond verandert in`{:class="block3events"} aan elke **drum** sprite met een `ga naar`{:class="block3motion"} blok om de positie te veranderen.

Je moet ook de beginpositie instellen `wanneer op de vlag wordt geklikt`{:class="block3events"}.

--- /task ---

--- task ---

**Opruimen:** als je tijd hebt, dan is het een goed idee om ervoor te zorgen dat de sprites in de sprite-lijst in een logische volgorde staan, te beginnen met de drums in de volgorde waarmee ze upgraden en vervolgens de knoppen in de juiste volgorde.

--- /task ---

--- task ---

**Debug:** Zorg er eerst voor dat je echt begrijpt wanneer de drums en knoppen getoond moeten worden en hoe de `slagen`{:class="block3variables"} variabele moet veranderen. Het is veel gemakkelijker om een project te debuggen als je weet wat het moet doen.

--- collapse ---
---
title: Mijn drum wordt niet correct weergegeven/verborgen
---

Tenzij het de eerste drum is, zou je drum een `wanneer op de vlag wordt geklikt`{:class="block3events"} script moeten hebben om `te verbergen`{:class="block3looks"}. En het zou een `wanneer ik signaal`{:class="block3events"} `deze drum` ontvang script moeten hebben om `te tonen`{:class="block3looks"}.

Controleer of de **Get** knop voor deze drum `hetzelfde bericht uitzendt`{:class="block3events"}.


--- /collapse ---

--- collapse ---
---
title: Mijn Get-knop wordt niet correct weergegeven/verborgen
---

Tenzij de knop voor de allereerste drum is, moet deze `verbergen`{:class="block3looks"} `wanneer op de vlag wordt geklikt`{:class="block3events"}. En `verschijnen`{:class="block3looks"} `wanneer ik`{:class="block3events"} het bericht ontvang voor de **vorige drum**. De **Get** knop moet `verschijnen`{:class="block3looks"} om de speler laten weten naar welke volgende upgrade ze werken.

--- /collapse ---

--- collapse ---
---
title: Ik kan een drum kopen als ik niet genoeg beats heb
---

Controleer of je het aantal `slagen`{:class="block3variables"} hebt gewijzigd `wanneer deze sprite op`{:class="block3events"} klikt in het script voor de **Get** knop voor de trommel.

--- /collapse ---

--- collapse ---
---
title: Het aantal beats verandert niet correct als ik een nieuwe drum krijg
---

Controleer of je `de beats hebt veranderd met`{:class="block3variables"} een negatief getal `wanneer op deze sprite wordt geklikt`{:class="block3events"} in het script van de **Get** knop voor de drum.

Zorg ervoor dat dit overeenkomt met het getal op het uiterlijk van de drum knop.

--- /collapse ---

--- /task ---

--- collapse ---
---
title: Voltooid project
---

Je kunt het [voltooide project hier](https://scratch.mit.edu/projects/707231411/){:target="_blank"} bekijken.

--- /collapse ---

**Tip:** als je echt in de war raakt, is het goed om de nieuwe drum en de bijbehorende knop te verwijderen en opnieuw te beginnen. Soms is het moeilijk om een bug te vinden.

--- save ---
