
--- question ---

---
legend: Question 3 of 3
---

Fe wnes di ddefnyddio'r sgript yma i reoli beth sy'n digwydd pan fydd y chwaraewr yn clicio ar y botwm i uwchraddio ei ddrwm:

```blocks3
when this sprite clicked
if <(beats)>  [29]> then 
hide
change [beats v] by [-30] 
broadcast (conga v) 
else
say [Not enough beats!] for [2] seconds 
end
```

Os mai gwerth y newidyn `curiadau`{:class="block3variables"} yw `29`, beth fydd yn digwydd pan fydd y chwaraewr yn clicio ar y botwm?

--- choices ---

- ( ) Bydd y corlun yn `cuddio`{:class="block3looks"}

  --- feedback ---

  Ddim yn hollol, mae bloc `cuddio`{:class="block3looks"} yn y sgript, ond ni fydd yn rhedeg gyda `curiadau`{:class="block3variables"} wedi osod i `29`. Cymer olwg eto ar y sgript.

  --- /feedback ---

- (x) Bydd botwm y corlun yn `dweud`{:class="block3looks"} `Dim digon o guriadau!`

  --- feedback ---

Cywir, mae'r amod yn gwirio os ydy `curiadau`{:class="block3variables"} yn fwy na `29`, ond mae `curiadau`{:class="block3variables"} yn hafal i `29` felly does gan y chwaraewr ddim digon.

  --- /feedback ---

- ( ) Bydd 30 yn cael ei dynnu o werth y newidyn `curiadau`{:class="block3variables"}

  --- feedback ---

  Na, bydd gwerth y newidyn `curiadau`{:class="block3variables"} yn aros yr un peth. Mae `curiadau`{:class="block3variables"} wedi'i osod i `29` sy'n golygu bod `curiadau`{:class="block3variables"} `> 29` yn anghywir, felly fydd rhan gyntaf y bloc `os`{:class="block3control"} ddim yn rhedeg.

  --- /feedback ---

- ( ) Dim byd

  --- feedback ---

  Na, bydd y sgript bob amser yn gwneud rhywbeth. Cymer olwg agosach i weld pa ran o'r sgript fydd yn rhedeg pan fydd gen ti `29` o `guriadau`{:class="block3variables"}.

  --- /feedback ---

--- /choices ---

--- /question ---
