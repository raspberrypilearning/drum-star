
--- question ---

---
legend: Question 3 of 3
---

ಆಟಗಾರ ಅವರ ಡ್ರಮ್‌ನ್ನು ಅಪ್‌ಗ್ರೇಡ್‌ ಮಾಡಲು ಬಟನ್‌ನ್ನು ಕ್ಲಿಕ್‌ ಮಾಡಿದಾಗ ಏನಾಗುತ್ತದೆ ಎಂಬುವುದನ್ನು ನಿಯಂತ್ರಿಸಲು ನೀವು ಈ ಬರಹವನ್ನು ಉಪಯೋಸಿದ್ದೀರಿ:

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

`beats`{:class="block3variables"} ವೇರಿಯೇಬಲ್‌ನ ಮೌಲ್ಯವು `29` ಆಗಿದ್ದರೆ, ಆಟಗಾರ ಬಟನ್‌ ಮೇಲೆ ಕ್ಲಿಕ್‌ ಮಾಡಿದಾಗ ಏನಾಗುತ್ತದೆ?

--- choices ---

- ( ) ಸ್ಪ್ರೈಟ್ `hide`{:class="block3looks"}ಮಾಡುತ್ತದೆ

  --- feedback ---

  ಅಷ್ಟು ಸರಿಯಲ್ಲ, ಬರಹದಲ್ಲಿ `hide`{:class="block3looks"} ಬ್ಲಾಕ್‌ ಇದೆ, ಆದರೆ ಅದು `29` `beats`{:class="block3variables"} ಜೊತೆ ರನ್‌ ಆಗುವುದಿಲ್ಲ. ಬರಹವನ್ನು ಮತ್ತೊಮ್ಮೆ ನೋಡಿ.

  --- /feedback ---

- (x) ಬಟನ್‌ ಸ್ಪ್ರೈಟ್ `say`{:class="block3looks"} `Not enough beats!`‌ ಹೇಳುತ್ತದೆ

  --- feedback ---

ಹೌದು, ಷರತ್ತು `beats`{:class="block3variables"} `29`ಕ್ಕಿಂತ ಹೆಚ್ಚಿದೆಯೇ, ಆದರೆ `beats`{:class="block3variables"} `29`ಗೆ ಸಮನಾಗಿದೆ, ಆದುದರಿಂದ ಆಟಗಾರನ ಬಳಿ ಸಾಕಷ್ಟು ಇಲ್ಲ ಎಂದು ಪರಿಶೀಲಿಸುತ್ತದೆ.

  --- /feedback ---

- ( ) 30 ಯನ್ನು `beats`{:class="block3variables"} ವೇರಿಯೇಬಲ್‌ನ ಮೌಲ್ಯದಿಂದ ಹೊರತೆಗೆಯಲಾಗುತ್ತದೆ

  --- feedback ---

  ಇಲ್ಲ, `beats`{:class="block3variables"} ವೇರಿಯೇಬಲ್‌ನ ಮೌಲ್ಯವು ಅಷ್ಟೇ ಇರುತ್ತದೆ. `beats`{:class="block3variables"} `29` ಅಂದರೆ `beats`{:class="block3variables"} `> 29` ತಪ್ಪು, ಆದುದರಿಂದ `if`{:class="block3control"} ಬ್ಲಾಕ್‌ನ ಮೊದಲ ಭಾಗದದಲ್ಲಿರುವ ಬ್ಲಾಕ್‌ಗಳು ರನ್‌ ಆಗುವುದಿಲ್ಲ.

  --- /feedback ---

- () ಏನೂ ಇಲ್ಲ

  --- feedback ---

  ಇಲ್ಲ, ಬರಹ ಯಾವಾಗಲೂ ಏನನ್ನಾದರೂ ಮಾಡುತ್ತದೆ. `29` `beats`{:class="block3variables"} ಇರುವಾಗ ಬರಹದ ಯಾವ ಭಾಗ ರನ್‌ ಆಗುತ್ತದೆ ಎಂದು ನೋಡಲು ಸೂಕ್ಷ್ಮವಾಗಿ ಗಮನಿಸಿ.

  --- /feedback ---

--- /choices ---

--- /question ---
