## アップグレード第二弾

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
あなたのドラムスキルは向上しています。 アップグレード第二弾の時がきまして！ このステップでは、追加するドラムを選びます。
</div>
<div>
![3 つのドラムがあるパーティーの背景を示すステージ](images/second-upgrade.png){:width="300px"}
</div>
</div>

--- task ---

**Drum-snare** スプライトを複製（ふくせい）します。

![](images/duplicate-snare-drum.png)

--- /task ---

**Drum Costumes** スプライトには、選択できるドラムコスチュームがたくさんあります。

--- task ---

**Drum Costumes** スプライトをクリックし、 **コスチューム** タブを選びます。

**選択:** 次のアップグレード用のドラム。 この例では、**Conga**を選びました。

選んだドラムの「たたいている」コスチュームと「たたいていない」コスチュームを新しい **Drum-snare2** スプライトにドラッグします。

![あるスプライトから別のスプライトにコスチュームをドラッグする方法を示すアニメーション画像。](images/drag-costumes.gif)

![コスチュームリストに 2 つのコスチュームが追加された新しいスプライトのペイントエディター。](images/drum-3-costumes.png)

--- /task ---

--- task ---

選んだコスチュームに合わせてドラムに名前をつけます。

![](images/drum-3-named.png)

--- /task ---

--- task ---

**コード**タブをクリックします。 コードを変更して、正しいコスチュームを使用し、新しいドラムのサウンドを選びます。

新しいドラムをクリックしたときにゲットするビート数を `5`に変えます。

![](images/drum-3-icon.png)

```blocks3
when this sprite clicked
+change [ビート数 v] by [5] //クリックするたび5ビートふやす
+switch costume to [ v] //たたいているコスチューム
+play drum [ v] for [0.25] beats //ドラム音
+switch costume to [ v] //たたいていないコスチューム
```

--- /task ---

--- task ---

新しいドラムをステージ上の位置にドラッグします。

![他のドラムの右側にある新しいドラム。](images/drum-3-positioned.png)

--- /task ---

次に、プレーヤーがこの新しいドラムにアップグレードできるようにするためのボタンが必要です。

--- task ---

**スネアをゲット** スプライトを複製します。

ステージの右下におきます。 その名前を `ゲット` それに新しいドラムの名前に変更します。

![スプライトのリストと'スネアをゲット’スプライトの複製 スプライト名が新しいドラムに合わせて変更され、ステージの右下に配置されました。](images/get-drum-3.png)

--- /task ---

--- task ---

ボタンコスチュームから **snare drum** を消します。 新しいドラムの「たたいていない」コスチュームをコピーして、ボタンコスチュームに貼り付けます。

**Text** ツールをクリックし、数値を `30` に変更して、新しいドラムのコストを表示します。

ボタンはこんな感じになります：

![選んだドラムの画像とテキストが 30 に更新された新しいボタンコスチュームが表示されているペイント エディター。](images/get-drum-copy.png)

--- /task ---


このボタンは、スタート時に `非表示`{:class="block3looks"} にし、プレーヤーがスネア ドラムにアップグレードしたときに `表示`{:class="block3looks"} するようにします。

--- task ---

![](images/get-drum-3-icon.png)

```blocks3
when flag clicked
- show
+ hide
```

**ヒント:** ブロックを削除するには、ブロックをブロックメニューにドラッグするか、右クリックして **ブロックの削除**を選びます。 パソコンの場合、ブロックをクリックしてから <kbd>削除</kbd> をタップしてブロックを削除することもできます。

--- /task ---

--- task ---

プレーヤーが **Drum -snare** ドラムをゲットしたときに次のアップグレードとして新しいドラム ボタンが表示されるように 、`メッセージを受け取ったとき`{:class="block3events"} のスクリプトを追加します。

![](images/get-drum-3-icon.png)

```blocks3
when I receive [スネア v] //前のドラムを買った時に表示する
show //次に買えるドラムのボタンを表示
```

--- /task ---

--- task ---

このドラムをゲットするのに必要なビート数と、プレーヤーがこのドラムを手に入れたときに減らすビート数を変えます。

プレーヤーが新しいドラムをゲットしたときに `送る`{:class="block3events"} メッセージも変えます。 新しいドラムの名前を使って新しいメッセージを作成します。

![](images/get-drum-3-icon.png)

```blocks3
when this sprite clicked
if <(ビート数)>  [29]> then //29にかえる
hide
change [ビート数 v] by [-30] //30にかえる
broadcast (conga v) //あなたの選んだドラム名に変更
else
say (join ((30) - (ビート数)) [ビート数がたりないよ！]) for [2] seconds
end
```

--- /task ---

--- task ---

新しいドラムの名前の `メッセージを送る`{:class="block3events"}ように`スネアを受け取ったとき`{:class="block3events"} のスクリプトを変えていきます。 プレーヤーが新しいドラムにアップグレードすると、そのドラムが `表示`{:class="block3looks"} されます。

![](images/drum-3-icon.png)

```blocks3
when I receive [コンガ v] //あなたの選んだドラム名に変更
show
```

--- /task ---

--- task ---

**Party** の背景を追加します。

プレーヤーが新しいドラムにアップグレードしたときに背景を切り替えるスクリプトをステージに追加します。

![](images/stage-icon.png)

```blocks3
when I receive [コンガ v] //あなたの選んだドラム名に変更
switch backdrop to (Party v)
```

--- /task ---

--- task ---

**テスト:** 緑の旗をクリックしてゲームをスタートし、新しいドラムを手に入れるのに十分なビートを獲得できるかテストします。

十分なビートをゲットする前にボタンをクリックするとどうなりますか?

--- /task ---

--- save ---
