## 跳んで、跳びまわって、跳びはねて、滑空する！

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
このステップでは、スタートからゴールのプラットフォームへジャンプするキャラクターの動きをコーディングします。 
</div>
<div>
![](images/jump-example.png){:width="300px"}
</div>
</div>

キャラクターをステージ上でジャンプさせます。 まだ落ちる心配はありません。

--- task ---

**選択：** キャラクターに合ったジャンプ音を追加します。

[[[generic-scratch3-sound-from-library]]]

次に、キャラクターがステージを飛び越えるように、キーボードの<kbd>スペース</kbd>バーを押すか、タブレットのステージをタップします。

[[[scratch3-top-down-jumping]]]

--- /task ---

--- task ---

**テスト：** <kbd>スペース</kbd>バーまたはステージをタップして、キャラクターがステージを飛び越えて**ゴール**のプラットフォームまでジャンプさせます。

キャラクターが3〜4回のジャンプでステージを飛び越えるまで、コードを調整します。

--- /task ---

**ヒント：** ゲームに`ずっと`{:class="block3control"}ブロックを持たせて、その内部の`もし`{:class="block3control"}条件文で重要な条件が真になったら何かを行うことはとても一般的です。

--- task ---

**デバッグ:**

--- collapse ---

---
title: 緑色の旗をクリックしても、スプライトがスタートのプラットフォームに移動しません
---

**キャラクター**のスプライトにセットアップスクリプトがあることを確認します。


```blocks3
when flag clicked // セットアップ
+go to (スタート v)
set [着地 v] to [0]
set size to (着地) %
+go to [front v] layer
show
broadcast (スタート v) // 他のスクリプトを開始する
```

`行く`{:class="block3motion"}ブロックの中の名前が、**スタート**スプライトの名前と一致していることを確認します。

`最前面へ移動する`{:class="block3looks"}ブロックがあることを確認します。 スプライトがスタートのプラットフォームの下にある可能性があります。

**キャラクター**のスプライトを隠していないことを確認します。 必要ならば、セットアップスクリプトに`表示する`{:class="block3looks"}ブロックを追加します。


--- /collapse ---

--- collapse ---

---
title: スプライトがスタートのプラットフォームの中央に移動しません
---

ペイントエディタで、スプライトのすべてのコスチュームが中央に配置されていることを確認します。

`他のスプライト`{:class="block3motion"}`へ行く`{:class="block3motion"}ブロックは、その中心が他のスプライトの中心と同じ位置になるようにスプライトを移動させます。 中心が間違ったところに設定されている場合、**キャラクター**はプラットフォームの中心に行きません。

--- /collapse ---

--- collapse ---

---
title: スプライトの向きやジャンプの方向が間違っています！
---

`度に向ける`{:class="block3motion"}ブロックを**キャラクター**のセットアップスクリプトに追加するか、スプライトペインで方向を変更します。 `回転方法`{:class="block3motion"}も変更する必要があるかもしれません。 また、スプライトの**コスチューム**が右を向くように回転することも必要かもしれません。

--- /collapse ---

--- collapse ---

---
title: スプライトが正しい距離をジャンプしません
---

**キャラクター**の`(ジャンプ)を受け取った`{:class="block3events"}スクリプトを見てください。 `動かす`{:class="block3motion"}ブロックの歩数、または`繰り返す`{:class="block3control"}ブロックの繰り返し数を変更してみてください。

```blocks3
+move [5] steps
```

上下ジャンプの数を変更する必要があることを忘れないでください。

--- /collapse ---

--- collapse ---

---
title: スプライトがジャンプするときに正しく拡大・縮小しません
---

**キャラクター**にある`旗が押されたとき`{:class="block3events"}スクリプトの最後に、`(開始)メッセージを送る`{:class="block3events"}ブロックを入れてください。

**キャラクター**の`(開始)メッセージを受け取った`{:class="block3events"}スクリプトを見てください。

2番目の`繰り返す`{:class="block3events"}ブロックの中の`大きさを変える`{:class="block3looks"}ブロックは、スプライトを小さくするために負の数（`-3`など）であることを確認します。

--- /collapse ---

ここで取り上げていないバグがある場合は、フィードバックでお知らせください。 自分でバグを修正した場合でも（よくできました！）お知らせください。

**ヒント：** 行き詰まった場合は、コードを声に出したり頭の中で読んだりして、それが行うだろうと自分が思うことと言っていることが同じか確認します。 バグが見つかるかもしれません。

--- /task ---

--- save ----
