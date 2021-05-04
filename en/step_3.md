## Get jumping!

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In this step, you will add a character and backdrop and create start and end platforms. 
</div>
<div>
<mark>Image, gif or video showing what they will achieve by the end of the step.</mark> ![](images/image.png){:width="300px"}
</div>
</div>


--- task ---

Get your character to go to the Start platform `when flag clicked`{:class="block3events"} and set the `size`{:class="block3looks"} and `go to front layer`{:class="block3looks"}. 

This is the set up code that gets your game ready at the start. 

**Tip:** It's a good idea to get it to `broadcast`{:class="block3events"} a `start`{:class="block3events"} message to let other scripts know when to start, otherwise they might start before everything has been setup.

--- collapse ---

---
title: Go to the start platform
---

```blocks3
when flag clicked // setup
go to (Start v)
set size to [25] %
go to [front v] layer
broadcast (start v) // start other scripts
```

--- /collapse ---
i
--- /task ---

You're going to make your character jump across the Stage. Don't worry about falling in yet.

--- task ---

Now make your character jump across the Stage.  Choose a jumping sound that suits your character.

[[[generic-scratch3-sound-from-library]]]

If you have a computer keyboard then you can use `when space key pressed`{:class="block3events"} to jump, if you are on a touchscreen you can make your character jump `when stage clicked`{:class="block3events"} by `broadcasting`{:class="block3events"} a `jump`{:class="block3events"} message.

[[[scratch3-top-down-jumping]]]

--- /task ---

--- task ---
**Test:** Tap the space bar or Stage to make your character jump across the Stage to the End platform.

Adjust your code until the character jumps across the stage in three or four jumps.

--- /task ---

When the player reaches the end platform, they should hear a reward sound and the platforms should stop moving.

**Tip:** It's really common for games to have a `forever`{:class="block3control"} block with `if`{:class="block3control"} statements inside it to do something when important conditions become true.

--- task ---

Add code to detect when your character reaches the End platform using `touching color`{:class="block3sensing"}.

--- collapse ---

---
title: End the game when touching colour
---

```blocks3
when I receive [start v]
forever
if <(size) = [100]> then // not in the air
if <touching color (#b89d2f) ?> then // at end
go to (End v)
play sound (Win v) until done
stop [all v]
end
end
end
```

--- /collapse ---

You will need to set the colour that is sensed to the colour of your End platform.

[scratch3-set-block-input-colour-with-eyedropper]

--- /task ---

--- task ---
**Test:** Click the green flag and then jump your character across the Stage. Make sure you hear the reward sound when you reach the End platform.
--- /task ---

--- save ----
