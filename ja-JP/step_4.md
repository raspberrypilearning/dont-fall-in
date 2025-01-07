## 勝者

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
このステップでは、プレーヤーが**ゴール**のプラットフォームに到達してゲームに勝つことを検出します。 
</div>
<div>
![](images/winner-aims.png){:width="300px"}
</div>
</div>

`ずっと`{:class="block3control"}ループを追加して、`もし`{:class="block3control"}で**キャラクター**がプラットフォームのレベルにあるかどうかと、そうであれば**ゴール**のプラットフォームに到達したか確認します。

--- task ---

**選択：** キャラクターに合った勝利の音を追加します。

--- /task ---

###  End the game when touching a coloured platform

--- task ---

Use a `touching color`{:class="block3sensing"} block to detect when your character sprite reaches the **End** platform.


```blocks3
when I receive [start v]
forever
if <(size) = (landed)> then // not in the air
if <touching color (#b89d2f) ?> then // at end
broadcast (stop v) // stop other sprites
stop [other scripts in sprite v] // stop jumping after win
go to (End v)
play sound (Win v) until done
stop [all v]
end
end
end
```

`スプライトの他のスクリプトを止める`{:class="block3control"}ブロックはキャラクターをジャンプさせるループを停止します。

A `broadcast (stop v)`{:class="block3events"} message is used when your game is finished so that other sprites can stop, but this sprite can do something such as playing a sound before it stops.

--- /task ---

Use the eyedropper to pick the colour of your **End** platform

--- task ---

```blocks3
<touching color (#20f73b) ?>

```
Click on the colour input to open the colour picker and then click on the eyedropper at the bottom.

![](images/eye-dropper-tool.png)

Move the mouse pointer over to the End platform on the Stage and click to select the colour.

![](images/eye-dropper-stage.png)

The colour in the block input will change to match the colour you chose. Click in the Code area to close the colour picker.

--- /task ---

--- task ---

**テスト：** 緑色の旗をクリックしてから、キャラクターをステージ上にジャンプさせます。 **ゴール**のプラットフォームに到達したときに勝利の音が聞こえることを確認してください。

**ヒント：** 次のステップに進んでコードを追加する前に、プロジェクトをテストしておくことはとても重要です。 コードを追加してしまうと、バグを見つけて修正するのが難しくなります。

--- /task ---


--- task ---

**デバッグ:**

--- collapse ---

---
title: スプライトがゴールのプラットフォームの中央に移動しません
---

ペイントエディターで、スプライトのすべてのコスチュームが中央に配置されていることを確認します。

`(他のスプライト)へ行く`{:class="block3motion"}ブロックは、その中心が他のスプライトの中心と同じ位置になるようにスプライトを移動させます。 中心が間違ったところに設定されている場合、**キャラクター**はプラットフォームの中心に行きません。

--- /collapse ---

--- collapse ---

---
title: ゲームがすぐ終了してしまいます
---

スプライトが**ゴール**のプラットフォームにいないときにゴールの色に触れていないことを確認します。プロジェクトの他の場所で同じ色を使用すると、キャラクターがすぐに死んでしまう可能性があります。

--- /collapse ---

--- collapse ---

---
title: ゴールのプラットフォームに着地しても音が鳴らない
---

**キャラクター**のスプライトをクリックしてから「音」タブをクリックします。 スプライトにゴールの音が追加されていることを確認してください。 **再生**ボタンをクリックしてコンピューターで音が鳴ることを確認します。

**コード**タブをクリックし、スプライトが**ゴール**のプラットフォームに到達したときに実行される、`音を鳴らす`{:class="block3sound"}ブロックに正しい音が含まれていることを確認します。

`色に触れた`{:class="block3sensing"}ブロックの色が正しいことを確認します。 よくわからない場合は、もう一度選択してください。 色は似ているように見えても同じではない場合があります。

```blocks3
when I receive [start v]
forever
if < (size) = (landed) > then // not in the air
+if <touching color (#b89d2f) ?> then // at end
broadcast (stop v) // stop other sprites
go to (End v)
+play sound (Win v) until done
stop [all v]
end
end
end
```

--- /collapse ---

ここで取り上げていないバグがある場合は、フィードバックでお知らせください。 自分でバグを修正した場合でも（よくできました！）お知らせください。

**ヒント：** 行き詰まった場合は、コードを声に出したり頭の中で読んだりして、それが行うだろうと自分が思うことと言っていることが同じか確認します。 バグが見つかるかもしれません。

--- /task ---

--- save ---
