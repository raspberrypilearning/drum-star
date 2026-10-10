## Next drum

--- task ---

プロジェクトに **Drum-snare** スプライトを追加して、ステージ上におきます。

![](images/snare-stage.png)

--- /task ---

--- task ---

**Drum-cymbal**スプライトから `このスプライトが押されたとき`{:class="block3events"}を **Drum-snare**スプライトにドラッグします。

--- /task ---

--- task ---

Change the costume and the drum sound for the **Drum-snare** sprite.

![](images/snare-icon.png)

```blocks3
when this sprite clicked
+switch costume to [drum-snare-b v] //hit costume
+play drum [(1) Snare Drum v] for [0.25] beats //drum sound
+switch costume to [drum-snare-a v] //not hit costume
```

--- /task ---

--- task ---

Change the number of beats earned to `2`:

```blocks3
when this sprite clicked
+change [beats v] by [2] //2 beats per click
switch costume to [drum-snare-b v] //hit costume
play drum [(1) Snare Drum v] for [0.25] beats //drum sound
switch costume to [drum-snare-a v] //not hit costume
```

--- /task ---

--- task ---

**テスト：**プロジェクトを実行します。

You should you earn 2 beats when you click on the snare drum.

--- /task ---

The next drum is not available when you start the project. It has to be earned with beats.

--- task ---

Add a script to the **Drum-snare** sprite to hide it at the start of the project:

```blocks3
when flag clicked
hide
```

--- /task ---

Add a button to show which drum is the next and how many beats it will cost.

--- task ---

**ゲット**スプライト を **複製（ふくせい）**します:

![](images/duplicate-get.png)

--- /task ---

--- task ---

Change the visibility to **Show**. ![](images/show.png)

--- /task ---

--- task ---

Change its name to `Get snare`.

--- /task ---

--- task ---

ステージの右下におきます。

![](images/get-snare.png)

--- /task ---

--- task ---

**Drum-snare** スプライトをクリックしてから、**コスチューム** タブをクリックします。

![](images/snare-icon.png)

Use the **Select** (arrow) tool to highlight the 'not hit' costume of your drum. **グループ化**アイコンをクリックしてから**コピー**アイコンをクリックします。

![](images/copy-costume.png)

--- /task ---

--- task ---

**スネアをゲット** スプライト をクリックし、 スネアのコスチュームを**貼り付け** ます。 ボタンに合わせてサイズや位置を調整しましょう。

![](images/paste-costume.png)

--- /task ---

--- task ---

**コード** タブをクリックして、プロジェクトのスタート時に **スネアゲット** スプライトを表示するスクリプトを追加します。

![](images/get-snare-icon.png)

```blocks3
when flag clicked
show
```

--- /task ---

The next drum can only be unlocked if the user has `10` or more beats.

--- task ---

Add this code to unlock the next drum `if`{:class="block3control"} the player has enough beats, or `say`{:class="block3looks"} `More beats needed!` if they do not have enough:

```blocks3
when this sprite clicked
if <(beats)>  [9]> then //if 10 or more beats
hide
change [beats v] by [-10] //take away the cost of upgrade
else
say [More beats needed!] for [2] seconds 
end
```

--- /task ---

--- task ---

`メッセージ`{:class="block3events"} ブロックを追加して、新しい `スネア` メッセージを送ります。

```blocks3
when this sprite clicked
if <(beats)>  [9]> then // if 10 or more beats
hide
change [beats v] by [-10] // take away the cost of upgrade
+ broadcast (snare v) // your drum name
else
say [More beats needed!] for [2] seconds
end
```

--- /task ---

--- task ---

**Drum-snare** のスプライトをクリックします。

![](images/snare-icon.png)

このスクリプトを追加します。

```blocks3
when I receive [snare v]
show
```

--- /task ---

--- task ---

**テスト：**プロジェクトを実行します。

You should not be able to unlock the next drum before you have enough beats.

--- /task ---

When you unlock new drums, you can play at bigger venues!

--- task ---

背景を追加します。 学校で 2 回目の演奏会を行うために、 **Chalkboard** を選びました。

**Tip:** Choose a venue that's a small step up from a bedroom. You want to save bigger venues for later!

--- /task ---

--- task ---

Click on the Stage.

![](images/stage-icon.png)

アップグレードメッセージを受け取った時に、 `背景を..にする`{:class="block3looks"}コードをステージに追加します。

```blocks3
when I receive [snare v]
switch backdrop to [Chalkboard v]
```

--- /task ---

--- task ---

**Test:** Run your project.

When you unlock the next drum: the snare should appear, the button disappears, the venue changes and the `beats`{:class="block3variables"} go down by `10`.

--- /task ---

--- save ---
