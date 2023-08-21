## アップグレード第一弾

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
アップグレードの第一弾を作りましょう。 **スネアをゲット** ボタンが最初に表示されるため、プレーヤーはどのドラムをめざしてプレーをしているのかがわかります。
</div>
<div>
![](images/first-upgrade.png){:width="300px"}
</div>
</div>

--- task ---

プロジェクトに **Drum-snare** スプライトを追加して、ステージ上におきます。

![](images/snare-stage.png)

--- /task ---

--- task ---

**Drum-cymbal**スプライトから `このスプライトが押されたとき`{:class="block3events"}を **Drum-snare**スプライトにドラッグします。

[[[scratch3-copy-code]]]

--- /task ---

--- task ---

コスチュームとドラムの音を変えます。

ゲットするビート数を `2`に変えます。

![](images/snare-icon.png)

```blocks3
when this sprite clicked
+change [beats v] by [2] //2 beats per click
+switch costume to [drum-snare-b v] //hit costume
+play drum [(1) Snare Drum v] for [0.25] beats //drum sound
+switch costume to [drum-snare-a v] //not hit costume
```

--- /task ---

--- task ---

**テスト：**プロジェクトを実行します。 スネアドラムをクリックしたときに 2 ビートをゲットできることを確認します。

--- /task ---

プロジェクトのスタート時には、アップグレードは使えないようにします。 ビートを稼いでゲットできるようにします。

--- task ---

プロジェクトのスタート時に、この **drum** スプライトを非表示にするスクリプトを追加します。

![](images/snare-icon.png)

```blocks3
when flag clicked
hide
```

--- /task ---

ボタンには、次のアップグレードオプションであるドラムと、それにかかるビート数を表示します。

--- task ---

**ゲット**スプライト を **複製（ふくせい）**します:

![](images/duplicate-get.png)

表示/非表示を **表示** に変更し、名前を `スネアをゲット`に変えます。 ステージの右下におきます。

![](images/get-snare.png)

--- /task ---

--- task ---

**Drum-snare** スプライトをクリックしてから、**コスチューム** タブをクリックします。 **選択** (矢印) ツールを使って、ドラムの叩いていないコスチュームをハイライト（強調表示）します。 **グループ化**アイコンをクリックしてから**コピー**アイコンをクリックします。

![](images/snare-icon.png)

![](images/copy-costume.png)

--- /task ---

--- task ---

**スネアをゲット** スプライト をクリックし、 スネアのコスチュームを**貼り付け** ます。 ボタンに合わせてサイズや位置を調整しましょう。

![](images/get-snare-icon.png)

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

アップグレードは、プレーヤーが `10` 以上のビートを持っているときだけにしか購入することができません。 [トンボを育てる](https://projects.raspberrypi.org/en/projects/grow-a-dragonfly){:target="_blank"} プロジェクトでは、`もし`{:class="block3control"} ブロックで決定を行うことについて学びました。

`もし ... でなければ`{:class="block3control"} ブロックは決定を行う時に使います。条件が `true（真）` か `false（偽）`によって別々の処理を実行します。

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
私たちは常に<span style="color: #0faeb0">**条件**</span>で判断しています。 起きたとき、朝'かどうか'{:class="block3control"}を確認します。 起き上がるか、 `でなければ`{:class="block3control"} また眠りに戻ります。 `もし... でなければ`{:class="block3control"} で行う決定は他に何か思いつきますか？ 
</p>

--- task ---

Add this code to get the upgrade `if`{:class="block3control"} the player has enough beats, or `say`{:class="block3looks"} `More beats needed!` if they are not able to upgrade:

![](images/get-snare-icon.png)

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

Instead of only telling the player they need **more** beats, you can tell the player exactly **how many more** beats are needed to get the upgrade.

A `join`{:class="block3operators"} block is used to concatenate, or 'link' two values together.

![](images/get-snare-icon.png)

--- task ---

Add this code to `join`{:class="block3operators"} the number of beats needed with the text you have used to tell the player they need more beats if they are not able to upgrade:

```blocks3
when this sprite clicked
if <(beats)>  [9]> then //if 10 or more beats
hide
change [beats v] by [-10] //take away the cost of upgrade
else
+ say (join ((10) - (beats)) [beats needed!]) for [2] seconds
end
```

--- /task ---

--- task ---

Add a `broadcast`{:class="block3events"} block to send a new `snare` message:

![](images/get-snare-icon.png)

```blocks3
when this sprite clicked
if <(beats)>  [9]> then // if 10 or more beats
hide
change [beats v] by [-10] // take away the cost of upgrade
+ broadcast [snare v] // your drum name
else
say (join ((10) - (beats)) [beats needed!]) for [2] seconds
end
```

--- /task ---

--- task ---

Click on the **Drum-snare** sprite. Add this script:

![](images/snare-icon.png)

```blocks3
when I receive [snare v]
show
```

--- /task ---

When you upgrade your equipment, you will be able to play at bigger venues.

--- task ---

Add another backdrop. We chose **Chalkboard** to play our second gig at school.

Add code to the Stage to `switch backdrop`{:class="block3looks"} when the upgrade message is received:

![](images/stage-icon.png)

```blocks3
when I receive [snare v]
switch backdrop to [Chalkboard v]
```

**Tip:** Choose a venue that's a small step up from the bedroom. You want to save bigger venues for later.

--- /task ---

--- task ---

**Test:** Run your project. Try and buy the snare upgrade before you have enough beats.

When you buy the upgrade check: the snare appears, the button disappears, the venue changes and the `beats`{:class="block3variables"} go down by `10`.

--- /task ---

--- save ---
