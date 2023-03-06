## Neidio, hopian, bownsio, neu gleidio!

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Yn y cam yma, byddi di'n codio dy gymeriad i neidio o'r platfformau dechrau i'r platfformau diwedd. 
</div>
<div>
![](images/jump-example.png){:width="300px"}
</div>
</div>

Rwyt ti'n mynd i wneud i dy gymeriad neidio ar draws y Llwyfan. Paid â phoeni am syrthio i mewn eto.

--- task ---

**Dewis:** Ychwanega sain neidio sy'n addas i dy gymeriad.

[[[generic-scratch3-sound-from-library]]]

Gwna i dy gymeriad neidio ar draws y Llwyfan drwy wasgu'r botwm <kbd>space</kbd> ar fysellfwrdd neu dapio'r Llwyfan ar dabled.

[[[scratch3-top-down-jumping]]]

--- /task ---

--- task ---

**Prawf:** Tapia'r botwm <kbd>space</kbd> neu'r Llwyfan i wneud i dy gymeriad neidio ar draws y Llwyfan i'r platfform **Diwedd**.

Addasa dy god nes bod y cymeriad yn neidio ar draws y Llwyfan mewn tair neu bedair naid.

--- /task ---

**Awgrym:** Mae'n arferol cael bloc `am byth`{:class="block3control"} mewn gêm gyda datganiadau `if`{:class="block3control"} y tu mewn iddo er mwyn gwneud rhywbeth pan ddaw amodau pwysig yn wir.

--- task ---

**Difa chwilod:**

--- collapse ---

---
title: Dydy fy nghorlun ddim yn mynd i'r platfform Dechrau pan fydda i'n clicio ar y faner werdd
---

Gwna'n siŵr fod gen ti sgript gosod ar dy gorlun **cymeriad**:


```blocks3
when flag clicked // gosod
+go to (Cychwyn v)
set [wedi glanio v] to [0]
set size to (wedi glanio) %
+go to [front v] layer
show
broadcast (cychwyn v) // dechrau sgriptiau eraill
```

Gwna'n siŵr fod yr enw yn y bloc `mynd i`{:class="block3motion"} yn cyfateb i enw dy gorlun **Dechrau**.

Gwna'n siŵr fod gen ti floc `mynd i'r haen flaen`{:class="block3looks"}. Efallai fod dy gorlun o dan y platfform Dechrau!

Gwna'n siŵr nad wyt ti wedi cuddio dy gorlun **cymeriad**. Ychwanega floc `dangos`{:class="block3looks"} i dy sgript gosod os oes angen.


--- /collapse ---

--- collapse ---

---
title: Dydy fy nghorlun ddim yn mynd i ganol y platfform Dechrau
---

Mae angen sicrhau bod dy holl wisgoedd corlun wedi'u canoli yn y golygydd Paent.

Mae'r bloc `mynd i`{:class="block3motion"} `gorlun arall`{:class="block3motion"} yn symud corlun fel bod ei ganol yn yr un safle â chanol y corlun arall. Os ydy eu canolau yn y lle anghywir, yna fydd dy **gymeriad** ddim yn mynd i ganol y platfformau.

--- /collapse ---

--- collapse ---

---
title: Mae fy nghorlun yn pwyntio neu'n neidio i'r cyfeiriad anghywir!
---

Ychwanega floc `pwyntio i gyfeiriad`{:class="block3motion"} i sgript gosod y **cymeriad**neu newid y cyfeiriad yn y cwarel corlun. Efallai bydd angen i ti hefyd newid yr `arddull cylchdroi`{:class="block3motion"}. Efallai bydd angen i ti hefyd gylchdroi **gwisg** dy gorlun fel ei fod yn wynebu i'r dde.

--- /collapse ---

--- collapse ---

---
title: Dydy fy nghorlun ddim yn neidio'r pellter cywir
---

Edrycha ar sgript `pan rwy'n derbyn (naid)`{:class="block3events"} dy **gymeriad**. Rho gynnig ar newid nifer y camau yn y blociau `symud`{:class="block3motion"}, neu nifer yr ailadroddiadau yn y bloc `ailadrodd`{:class="block3control"}.

```blocks3
+move [5] steps
```

Cofia, bydd angen i ti newid y rhifau ar gyfer rhannau i fyny ac i lawr y naid.

--- /collapse ---

--- collapse ---

---
title: Dydy fy nghorlun ddim yn tyfu nac yn crebachu'n gywir pan mae'n neidio
---

Gwna'n siŵr fod gen ti floc `darlledu (dechrau)`{:class="block3events"} ar ddiwedd sgript `pan fydd y fflag wedi'i chlicio`{:class="block3events"} dy **gymeriad**.

Edrycha ar sgript `pan rwy'n derbyn (dechrau)`{:class="block3events"} dy **gorlun**.

Gwna'n siŵr fod gan y bloc `newid maint`{:class="block3looks"} yn yr ail floc `ailadrodd`{:class="block3events"} rif negatif i wneud y corlun yn llai, megis `-3`.

--- /collapse ---

Os oes gen ti chwilen nad ydyn ni wedi ymdrin â hi yma, rho wybod i ni yn yr adborth. Os wnes di drwsio'r chwilen dy hun (da iawn!), rho wybod i ni am hynny hefyd.

**Awgrym:** Os wyt it methu datrys dy broblem, rho gynnig ar ddarllen dy god yn uchel neu yn dy ben i wneud yn siŵr ei fod yn dweud beth rwyt ti'n meddwl. Efallai byddi di'n dod o hyd i'r chwilen.

--- /task ---

--- save ----
