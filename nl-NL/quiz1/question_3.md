
--- question ---

---
legend: Vraag 3 van 3
---

Je hebt dit script gebruikt om te bepalen wat er gebeurt wanneer de speler op de knop klikt om de drum te upgraden:

```blocks3
when this sprite clicked
if <(beats)>  [29]> then 
hide
change [beats v] by [-30] 
broadcast [conga v] 
else
say [Niet genoeg beats!] for [2] seconds 
end
```

Wat gebeurt er als de waarde van de `beats`{:class="block3variables"} variabele `29` is?

--- choices ---

- ( ) de sprite zal zich `verbergen`{:class="block3looks"}

  --- feedback ---

  Niet helemaal, er is een `verbergen`{:class="block3looks"} blok in het script, maar het zal niet draaien met `29` `beats`{:class="block3variables"}. Bekijk het script opnieuw.

  --- /feedback ---

- (X) de knop sprite zal `zeggen`{:class="block3looks"} `niet genoeg beats!`

  --- feedback ---

Ja, de voorwaarde controleert of `beats`{:class="block3variables"} groter is dan `29`, maar `beats`{:class="block3variables"}is gelijk aan `29` zodat de speler niet genoeg beats heeft.

  --- /feedback ---

- ( ) 30 wordt verwijderd van de waarde van de `beats`{:class="block3variables"} variabele

  --- feedback ---

  Nee, de waarde van de `beats`{:class="block3variables"} variabele blijft hetzelfde. `beats`{:class="block3variables"} is `29` wat betekent dat `beats`{:class="block3variables"} `> 29` niet waar is, dus de blokken in het eerste deel van het `als`{:class="block3control"} blok zullen niet worden uitgevoerd.

  --- /feedback ---

- ( ) niets

  --- feedback ---

  Nee, het script zal altijd iets doen. Bekijk eens welk deel van het script wordt uitgevoerd als je `29` `beats`{:class="block3variables"} hebt.

  --- /feedback ---

--- /choices ---

--- /question ---
