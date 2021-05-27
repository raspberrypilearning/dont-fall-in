## Reflection

Well done, you have learned a lot! Now it's time to reflect - reflecting is an important part of learning because it helps make new connections in your brain.

You learned some useful ways to combine the blocks you have learned about to make a game, including:
+ Using `forever`{:class="block3control"} block with `if`{:class="block3control"} statements to detect important **conditions** in your game and take action,
+ Broadcasting a `start`{:class="block3control"} message after setting up your character so everything is ready when you start the game,
+ Broadcasting a `stop`{:class="block3control"} message when you detect a game end **condition** such as winning or losing so that other script can stop and you can play a sound or do an animation before `stop [all]`{:class="block3control"}.

Answer the three questions below to reflect on what you've learned.

After each question, press submit. You will be guided towards the correct answer. You can do this activity as many times as you want to.

Have fun!

--- question ---

---
legend: Question 1 of 3
---

![The Stagee of a lava jumping game. The character is on the end platform, a golden door.](images/quiz-lava-stage.png)

You win this game by reaching the golden door and lose if you land in the lava pit. The game isn't working, how could you fix it?

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

- ( ) Change the colour in the 'check lose' condition.

  --- feedback ---

Close. The 'check lose' condition doesn't have the right colour, but just changing that won't make the game work.

  --- /feedback ---

- ( ) Change the colour in the 'check win' condition.

  --- feedback ---

Close. The 'check win' condition doesn't have the right colour, but just changing that won't make the game work.

  --- /feedback ---

- (x) Swap the colours in the 'check win' and 'check lose' conditions.

  --- feedback ---

Yes. The 'check lose' and 'check win' conditions have the colours the wrong way round! The player will will when they fall in the lava and lose when they reach the golden door! Swapping the conditions will fix this.

  --- /feedback ---

--- /choices ---

--- /question ---
