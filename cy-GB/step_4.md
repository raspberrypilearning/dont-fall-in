## Enillydd

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Yn y cam yma, byddi di'n canfod y chwaraewr yn cyrraedd y platfform **Diwedd** i ennill y gêm. 
</div>
<div>
![](images/winner-aims.png){:width="300px"}
</div>
</div>

Rwyt ti'n mynd i ychwanegu dolen `am byth`{:class="block3control"} sy'n gwirio a ydy dy **gymeriad** ar lefel y platfform, ac os felly, `os`{:class="block3control"} yw wedi cyrraedd y platfform **Diwedd**.

--- task ---

**Dewis:** Ychwanega sain ennill i dy gymeriad.

--- /task ---

--- task ---

Ychwanega god i ganfod pan fydd dy gymeriad yn cyrraedd y platfform **Diwedd** gan ddefnyddio `cyffwrdd lliw`{:class="block3sensing"}.

--- collapse ---

---
title: Gorffen y gêm wrth gyffwrdd lliw
---

**Cymeriad**:

```blocks3
when I receive [start v]
forever
if <(size) = (wedi glanio)> then // pan nad yw yn yr awyr
if <touching color (#b89d2f) ?> then // ar y diwedd
broadcast (stopio v) // rhwystro corluniau eraill
stop [other scripts in sprite v] // rhoi'r gorau i neidio ar ôl ennill
go to (Diwedd v)
play sound (Win v) until done
stop [all v]
end
end
end
```

Mae'n syniad `darlledu`{:class="block3events"} neges 'stop' i roi gwybod i gorluniau eraill fod y gêm wedi dod i ben. Mae'r bloc `aros sgriptiau eraill yn y ciplun`{:class="block3control"} yn stopio'r ddolen sy'n gwneud i'r cymeriad neidio.

--- /collapse ---

Bydd angen i ti osod y lliw sy'n cael ei synhwyro i liw dy blatfform **Diwedd**.

[[[scratch3-set-block-input-colour-with-eyedropper]]]

**Awgrym:** Mae'n syniad da `darlledu`{:class="block3events"} neges `dechrau`{:class="block3events"} ar ddiwedd dy sgript gosod i roi gwybod i sgriptiau eraill pryd i ddechrau, fel arall efallai byddan nhw'n dechrau cyn bod popeth yn barod.

--- /task ---

--- task ---

**Prawf:** Clicia'r faner werdd ac wedyn neidio dy gymeriad ar draws y Llwyfan. Gwna'n siŵr dy fod ti'n clywed y sain ennill pan fyddi di'n cyrraedd y platfform **Diwedd**.

**Awgrym:** Mae'n bwysig iawn dy fod yn profi dy brosiect cyn symud i'r cam nesaf ac ychwanegu mwy o god. Mae'n anoddach dod o hyd i chwilod a'u trwsio pan fyddi di wedi ychwanegu mwy o god.

--- /task ---


--- task ---

**Difa chwilod:**

--- collapse ---

---
title: Dydy fy nghorlun ddim yn mynd i ganol y platfform Diwedd
---

Mae angen sicrhau bod dy holl wisgoedd corlun wedi'u canoli yn y golygydd Paent.

Mae'r bloc `mynd i (corlun arall)`{:class="block3motion"} yn symud corlun fel bod ei ganol yn yr un safle â chanol y corlun arall. Os ydy eu canolau yn y lle anghywir, yna fydd dy **gymeriad** ddim yn mynd i ganol y platfformau.

--- /collapse ---

--- collapse ---

---
title: Mae'r gêm yn dod i ben yn rhy fuan
---

Gwna'n siŵr nad ydy dy gorlun yn cyffwrdd â'r lliw Diwedd pan nad yw ar y platfform **Diwedd** - os wyt ti'n defnyddio'r un lliw mewn man arall yn dy brosiect, yna gallai dy gymeriad farw'n rhy fuan.

--- /collapse ---

--- collapse ---

---
title: Dydy'r sain ddim yn chwarae pan fydda i'n glanio ar y platfform End
---

Clicia ar dy gorlun **cymeriad** ac yna'r tab 'Seiniau'. Gwna'n siŵr dy fod wedi ychwanegu'r sain Diwedd at dy gorlun. Clicia'r botwm **Chwarae** i sicrhau bod y sain yn gweithio ar dy gyfrifiadur.

Clicia'r tab **Cod** a gwirio fod y sain gywir yn y bloc `chwarae sain`{:class="block3sound"} sy'n rhedeg pan fydd y corlun yn cyrraedd y platfform **Diwedd**.

Gwna'n siŵr fod y lliw yn gywir yn y bloc `cyffwrdd lliw`{:class="block3sensing"}. Dewisa'r lliw eto os nad wyt ti'n siŵr. Weithiau mae lliwiau'n edrych yn debyg ond dydyn nhw ddim yr un fath.

```blocks3
when I receive [start v]
forever
if < (size) = (wedi glanio) > then // pan nad yw yn yr awyr
+if <touching color (#b89d2f) ?> then // ar y diwedd
broadcast (stopio v) // rhwystro corluniau eraill
go to (Diwedd v)
+play sound (Win v) until done
stop [all v]
end
end
end
```

--- /collapse ---

Os oes gen ti chwilen nad ydyn ni wedi ymdrin â hi yma, rho wybod i ni yn yr adborth. Os wnes di drwsio'r chwilen dy hun (da iawn!), rho wybod am hynny i ni hefyd.

**Awgrym:** Os wyt ti methu datrys dy broblem, rho gynnig ar ddarllen dy god yn uchel neu yn dy ben i wneud yn siŵr ei fod yn dweud yr hyn rwyt ti'n meddwl. Efallai byddi di'n dod o hyd i'r chwilen.

--- /task ---

--- save ---
