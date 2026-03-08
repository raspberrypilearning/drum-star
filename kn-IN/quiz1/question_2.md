
--- question ---

---
legend: Question 2 of 3
---

ಪ್ರಾಜೆಕ್ಟ್‌ ಒಂದರಲ್ಲಿ ಬಳಕೆದಾರರನ್ನು ಅವರ ಹೆಸರನ್ನು ಕೇಳಲು `ask`{:class="block3sensing"} ಬರಹ ಇದೆ:

```blocks3
when flag clicked
set [name v] to [???] 
ask [What's your name?] and wait 
set [name v] to (answer)
```

![](images/q1-chatbot.png)

ಆಟಗಾರ ಟಿಕ್ (ಪರಿಶೀಲನಾ ಗುರುತು) ಮೇಲೆ ಕ್ಲಿಕ್‌ ಮಾಡಿದ ಮೇಲೆ ಮತ್ತು ಬರಹ ಮುಗಿದಾಗ `name`{:class="block3variables"} ವೇರಿಯೇಬಲ್‌ನ ಮೌಲ್ಯ ಏನಾಗಿರುತ್ತದೆ?

--- choices ---

- ( )  name

  --- feedback ---

ಇಲ್ಲ, `name`{:class="block3variables"} ಎಂದರೆ ವೇರಿಯೇಬಲ್‌ನ್ನು ಏನು ಎಂದು ಕರೆಯುವುದು.

  --- /feedback ---

- ( ) ???

  --- feedback ---

ಇಲ್ಲ, `???` ಎಂದರೆ `ask`{:class="block3sensing"} ಬ್ಲಾಕ್‌ ರನ್‌ ಆಗುವ ಮುಂಚಿನ `name`{:class="block3variables"} ವೇರಿಯೇಬಲ್‌ನ ಮೌಲ್ಯ.

  --- /feedback ---

- ( ) answer

  --- feedback ---

ಇಲ್ಲ, ನೀವು `ask`{:class="block3sensing"} ಪ್ರಶ್ನೆಯನ್ನು ಕೇಳಿದಾಗ ಬಳಕೆದಾರ ಟೈಪ್‌ ಮಾಡುವ ಉತ್ತರವನ್ನು ಸಂಗ್ರಹಣೆ ಮಾಡಲು ಸ್ಕ್ರಾಚ್‌ ಉಪಯೋಗಿಸುವ ಅದರ ಭಾಗವಾಗಿರುವ `answer`{:class="block3sensing"}‌ ವೇರಿಯೇಬಲ್. --- /feedback ---

- (x) Bobo

  --- feedback ---

ಹೌದು, `set [name v] to`{:class="block3variables"} ಬ್ಲಾಕ್‌ `name`{:class="block3variables"}ವೇರಿಯೇಬಲ್‌ನ **ಮೌಲ್ಯ**ವನ್ನು `answer`{:class="block3sensing"}ನ ಮೌಲ್ಯಕ್ಕೆ ಹೊಂದಿಸುತ್ತದೆ, ಅದು ಬಳಕೆದಾರ ಟೈಪ್‌ ಮಾಡಿದ ಪಠ್ಯವಾಗಿರುತ್ತದೆ.

Stage ಮೇಲೆ `Bobo` ಮೌಲ್ಯವನ್ನೂ ಸಹ ತೋರಿಸಲಾಗುತ್ತದೆ.

  --- /feedback ---

--- /choices ---

--- /question ---
