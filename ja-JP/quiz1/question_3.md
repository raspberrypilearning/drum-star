
--- question ---

---
凡例：質問3/3
---

このスクリプトを使用して、プレーヤーがボタンをクリックしてドラムをアップグレードしたときの動作を制御しました。

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

変数 `ビート数`{:class="block3variables"}の値が `29`の場合、プレイヤーがボタンをクリックするとどうなるでしょうか？

--- choices ---

- ( ) スプライトが `非表示`{:class="block3looks"}になる。

  --- feedback ---

  いいえ。 このスクリプトの中に`非表示`{:class="block3looks"}のブロックはありますが、 `29`の `ビート数`{:class="block3variables"}では実行されません。 もう一度スクリプトを見てみましょう。

  --- /feedback ---

- (x) ボタンのスプライトが、 `ビート数がたりないよ！` `という`{:class="block3looks"}。

  --- feedback ---

正解です。 `ビート数`{:class="block3variables"} が `29`より大きいかチェックしますが、`ビート数`{:class="block3variables"}が `29`では十分ではありません。

  --- /feedback ---

- ( ) 変数 `ビート数`{:class="block3variables"} の値が30少なくなります。

  --- feedback ---

  いいえ、変数`ビート数`{:class="block3variables"}は、同じ値のままです。 `ビート数`{:class="block3variables"} が `29` ということは、 `ビート数`{:class="block3variables"}が `> 29` であることが偽（ぎ）なので、 `if`{:class="block3control"} ブロックの最初のぶぶんは実行されません。

  --- /feedback ---

- ( ) 何も起こらない。

  --- feedback ---

  いいえ、スクリプトは常に何かを行います。 `ビート数`{:class="block3variables"}が`29` の時に、なにが実行されるのかをよく見ましょう。

  --- /feedback ---

--- /choices ---

--- /question ---
