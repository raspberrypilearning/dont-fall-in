## ふりかえり

3つの質問に答えてください。 あなたを正解に導くヒントがあります。

各質問に回答したら、**答えを確認する**をクリックしてください。

お楽しみください！

--- question ---

---
legend: 質問1/3
---

![溶岩ジャンプゲームのステージ。 キャラクターがゴールのプラットフォームである黄金の扉にいる。](images/quiz-lava-stage.png)

黄金の扉に到達するとこのゲームに勝ち、溶岩ピットに着地すると負けとなります。 このゲームはうまく動きません。 どう修正したらよいでしょう？

```blocks3
when flag clicked
go to (Start v)
broadcast (start v)
```

```blocks3
when I receive [start v]
forever
if <touching color (#fff700) ?> then // check lose
broadcast (stop v) // stop other sprites
play sound (Lose v) until done
stop [all v]
end
if <touching color (#ff0000) ?> then // check win
broadcast (stop v) // stop other sprites
play sound (Win v) until done
stop [all v]
end
```


--- choices ---

- ( ) 「負けをチェックする」条件の色を変更する

  --- feedback ---

惜しい！ 「負けをチェックする」条件は正しい色ではありませんが、それを変更するだけではゲームはうまく動きません。

  --- /feedback ---

- ( ) 「勝ちをチェックする」条件の色を変更する

  --- feedback ---

惜しい！ 「勝ちをチェックする」条件は正しい色ではありませんが、それを変更するだけではゲームはうまく動きません。

  --- /feedback ---

- (x) 「勝ちをチェックする」と「負けをチェックする」条件の色を入れ替える

  --- feedback ---

正解！ 「勝ちをチェックする」と「負けをチェックする」条件の色が入れ替わっています。 プレイヤーは溶岩に落ちたときに勝ち、黄金の扉に到達したときに負けてしまいます！ 条件を交換してこれを修正します。

  --- /feedback ---

--- /choices ---

--- /question ---
