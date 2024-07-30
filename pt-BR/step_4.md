## Winner

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In this step, you will detect the player reaching the **End** platform to win the game. 
</div>
<div>
![](images/winner-aims.png){:width="300px"}
</div>
</div>

You're going to add a `forever`{:class="block3control"} loop that checks if your **character** is at platform level, and if so, `if`{:class="block3control"} it has reached the **End** platform.

--- task ---

**Choose:** Add a winning sound to your character.

--- /task ---

--- task ---

Add code to detect when your character reaches the **End** platform using `touching color`{:class="block3sensing"}.

--- collapse ---

---
title: End the game when touching colour
---

**Character**:

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

It's a good idea to `broadcast`{:class="block3events"} a 'stop' message to let other sprites know the game has ended. The `stop other scripts in sprite`{:class="block3control"} block stops the loop that makes the character jump.

--- /collapse ---

You will need to set the colour that is sensed to the colour of your **End** platform.

[[[scratch3-set-block-input-colour-with-eyedropper]]]

**Tip:** It's a good idea to `broadcast`{:class="block3events"} a `stop`{:class="block3events"} message when you detect that your game is finished so that other sprites can stop, but this sprite can do something such as playing a sound before it stops.

--- /task ---

--- task ---

**Test:** Click the green flag and then jump your character across the Stage. Make sure you hear the winning sound when you reach the **End** platform.

**Tip:** It's really important that you test your project before moving to the next step and adding more code. It's harder to find and fix bugs when you have added more code.

--- /task ---


--- task ---

**Depurar:**

--- collapse ---

---
title: My sprite doesn't go to the centre of the End platform
---

You need to make sure all your sprite costumes are centered in the Paint editor.

The `go to (other sprite)`{:class="block3motion"} block moves a sprite so that it's centre is in the same position as the centre of the other sprite. If their centres are in the wrong place, then your **character** won't go to the centre of the platforms.

--- /collapse ---

--- collapse ---

---
title: The game ends too soon
---

Check that your sprite isn't touching the End colour when it's not on the **End** platform — if you use the same colour elsewhere in your project, then your character could die too soon.

--- /collapse ---

--- collapse ---

---
title: The sound doesn't play when I land on the End platform
---

Click on your **character** sprite and then the 'Sounds' tab. Make sure you have added the End sound to your sprite. Click on the **Play** button to make sure sound is working on your computer.

Click on the **Code** tab and check that the correct sound is in the `play sound`{:class="block3sound"} block that runs when the sprite reaches the **End** platform.

Make sure the colour is correct in the `touching colour`{:class="block3sensing"} block. Select it again if you're not sure. Sometimes colours look similar but aren't the same.

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

If you have a bug that we haven't covered here, then let us know in the feedback. If you fixed the bug yourself (well done!), let us know that too.

**Tip:** If you're stuck, try reading your code out loud or in your head to make sure it says what you think it does. You might find the bug.

--- /task ---

--- save ---
