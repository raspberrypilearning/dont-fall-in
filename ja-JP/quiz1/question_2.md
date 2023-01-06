
--- question ---

---
legend: 質問2/3
---

以下は移動するプラットフォームのコードです。

```blocks3
when I receive [start v]
forever
move [20] steps
if on edge, bounce
end
```

ゲームが難しすぎて楽しくありません。 何をしたらプレイしやすくなるでしょう？

--- choices ---

- (x) `動かす`{:class="block3motion"}ブロックの数字を**小さい**数字に変更する

  --- feedback ---

その通りです。 数字を小さくすると、`ずっと`{:class="block3control"}ループが実行されるたびにプラットフォームが移動する歩数が少なくなるため、プラットフォームの移動が遅くなります。 これで着地しやすくなります。

  --- /feedback ---

- ( ) `動かす`{:class="block3motion"}ブロックの数字を**大きい**数字に変更する

  --- feedback ---

`ずっと`{:class="block3control"}ループが実行されるたびにより多くの歩数を移動させると、プラットフォームの移動が速くなります。 これでフォームが着地しにくくなります。

  --- /feedback ---

--- /choices ---

--- /question ---
