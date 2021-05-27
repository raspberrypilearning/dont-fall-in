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

<mark>Add screenshot of lava jumping game</mark>

You win this game by reaching the golden door and lose if you land in the lava pit. The game isn't working, how could you fix it?

```blocks3
when flag clicked
go to (Start v)
broadcast (start v)
```

<mark>Choose colour to match screenshot</mark>

```blocks3
when I receive [start v]
forever
if <touching color (#b89d2f) ?> then // check lose
broadcast (stop v) // stop other sprites
play sound (Lose v) until done
stop [all v]
if <touching color (#b89d2f) ?> then // check win
broadcast (stop v) // stop other sprites
play sound (Win v) until done
stop [all v]
end
```


--- choices ---

- ( ) Change the colour in the 'check lose' condition.

  --- feedback ---

  --- /feedback ---

- (x) Change the colour in the 'check win' condition.

  --- feedback ---

  --- /feedback ---

- ( ) Swap the colours in the 'check win' and 'check lose' conditions.

  --- feedback ---

  --- /feedback ---

--- /choices ---

--- /question ---
