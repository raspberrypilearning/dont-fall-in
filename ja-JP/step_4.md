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

--- task ---

`色に触れた`{:class="block3sensing"}を使用して、キャラクターが**ゴール**のプラットフォームに到達したことを検出するコードを追加します。

--- collapse ---

---
title: 色に触れたらゲームが終了します
---

**キャラクター**:

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

「停止」`メッセージを送る`{:class ="block3events"}でゲームが終了したことを他のスプライトに知らせるのがよいでしょう。 `スプライトの他のスクリプトを止める`{:class="block3control"}ブロックはキャラクターをジャンプさせるループを停止します。

--- /collapse ---

色は**ゴール**のプラットフォームの色に合わせる必要があります。

[[[scratch3-set-block-input-colour-with-eyedropper]]]

**ヒント：** ゲームが終了したことを検出したら、`停止`{:class="block3events"}`メッセージを送る`{:class="block3events"}とよいでしょう。そうすれば、他のスプライトを停止させて、今のスプライトが停止する前に音を再生するといった何かを行えます。

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
