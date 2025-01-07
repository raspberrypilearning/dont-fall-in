## Dewis dy thema

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Yn y cam yma, byddi di'n ychwanegu cymeriad a chefnlen, ac yn creu platfformau dechrau a diwedd. 
</div>
<div>
![](images/setup-example.png){:width="300px"}
</div>
</div>

--- task ---

Agora [brosiect Scratch newydd](http://rpf.io/scratch-new){:target="_blank"} a dileu corlun y gath. Bydd Scratch yn agor mewn tab arall ar y porwr.

--- /task ---

--- task ---

Crea gefndir lliw solet.

[[[scratch-paint-single-colour-backdrop]]]

--- /task ---

--- task ---

**Dewis:** Fydd dy gymeriad yn symud o'r chwith i'r dde, neu o'r gwaelod i'r brig?

![](images/direction-examples.png)

--- /task ---

--- task ---

Paentia gorlun platfform **Dechrau** newydd.

Dechreua gyda siâp un lliw syml. You can turn the outline off by choosing the red diagonal line.

![](images/no-outline.png)

Galli di ychwanegu mwy o fanylion nes ymlaen.

Canola dy wisg yn y Golygydd paent.

[[[scratch-crosshair]]]

Gosoda dy gorlun platfform **Dechrau** lle rwyt ti am i dy gymeriad ddechrau'r gêm.

--- /task ---

--- task ---

Crea gorlun platfform **Diwedd** syml. Galli di ychwanegu rhagor o fanylion nes ymlaen.

Canola dy wisg yn y Golygydd paent.

Gosoda dy gorlun platfform **Diwedd** lle rwyt ti am i dy gymeriad orffen y gêm.

--- /task ---

--- task ---

Crea gorlun **cymeriad**.

**Dewis:** Wyt ti am ychwanegu neu beintio corlun **cymeriad**?

Efallai hoffet ti ychwanegu corlun **cymeriad** o'r brig i lawr fel **Tatiana**, **Taylor**, neu **Trisha**.

![Delwedd o'r corluniau o'r brig i lawr sydd ar gael yn Scratch](images/top-down-sprites.png)

Neu, gallet ti beintio dy gorlun **cymeriad** dy hun. Dechreua gyda siapiau syml ac ychwanega'r manylion yn ddiweddarach. Creua dy wisg newydd yn y Golygydd Paent.

[[[generic-scratch3-draw-sprite]]]

--- /task ---

--- task ---

Mae angen sgript dechrau ar dy gorlun **cymeriad** er mwyn rhoi popeth yn ei le ar gyfer dechrau'r gêm.

Make a `variable`{:class="block3variables"} called `landed`, and set it to the size your sprite should be when it has landed and is not jumping.

Get your character to go to the **Start** `when flag clicked`{:class="block3events"}. Add a `go to front layer`{:class="block3looks"} block, so your character is on top of the platforms.

**Character:**

```blocks3
when flag clicked // setup
go to (Start v)
set [landed v] to [40] // size when not jumping
set size to (landed) % // not jumping
go to [front v] layer
show
broadcast (start v) // start other scripts
```

**Tip:** Uncheck the `landed`{:class="block3variables"} variable in the `Variables`{:class="block3variables"} Blocks menu so that it doesn't show on the Stage. The user doesn't need to see this variable.

**Awgrym:** Mae'n syniad `darlledu`{:class="block3events"} neges `dechrau`{:class="block3events"} ar ddiwedd dy sgript gosod i roi gwybod i sgriptiau eraill pryd i ddechrau, fel arall efallai byddan nhw'n dechrau cyn bod popeth yn barod.

--- /task ---

--- task ---

**Difa chwilod:**

--- collapse ---

---
title: Mae fy nghorlun yn pwyntio i'r cyfeiriad anghywir
---

Galli di ddefnyddio'r briodwedd **Cyfeiriad** yn y cwarel Sprite i reoli'r cyfeiriad mae'r corlun yn pwyntio iddo. Tro'r olwyn i wneud i'r corlun bwyntio i'r cyfeiriad sydd ei angen arnat.

![Y cwarel corluniau gyda'r briodwedd cyfeiriad wedi'i dewis. Neidlen gydag olwyn gyfeirio sy'n cael ei defnyddio i addasu'r cyfeiriad y mae'r corlun yn pwyntio iddo.](images/direction-property.png)

--- /collapse ---

--- /task ---

--- task ---

Rho deitl i dy brosiect sy'n disgrifio dy gêm.

--- /task ---

--- save ---
