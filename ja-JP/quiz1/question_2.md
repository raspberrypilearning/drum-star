
--- question ---

---
legend: Question 2 of 3
---

このプロジェクトには 、名前を質問するために、`..と聞いて待つ`{:class="block3sensing"} スクリプトがあります:

```blocks3
when flag clicked
set [name v] to [???] 
ask [What's your name?] and wait 
set [name v] to (answer)
```

![](images/q1-chatbot.png)

プレーヤーがチェック (チェックマーク) をクリックしてスクリプトが終了した後、 変数`名前`{:class="block3variables"} の値はどうなりますか?

--- choices ---

- ( )  名前

  --- feedback ---

いいえ、 `名前`{:class="block3variables"} は変数の名前です。

  --- /feedback ---

- ( ) ???

  --- feedback ---

いいえ、 `???` は、 `...と聞いて待つ`{:class="block3sensing"} ブロックが実行される前の変数 `名前`{:class="block3variables"} の値です。

  --- /feedback ---

- ( ) 答え

  --- feedback ---

いいえ、`答え`{:class="block3sensing"} は、`...と聞いて待つ`{:class="block3sensing"}の質問に対してプレーヤーが入力した答えを保存するためにScratchが使用する組み込み変数です。 --- /feedback ---

- (x) ボボ

  --- feedback ---

正解です。 `変数[名前v]を...にする`{:class="block3variables"} ブロックは、 変数`名前`{:class="block3variables"}の **値**にプレーヤーが入力したテキストである `答え`{:class="block3sensing"} の値にセットします。

`ボボ` という値は、ステージにも表示されます。

  --- /feedback ---

--- /choices ---

--- /question ---
