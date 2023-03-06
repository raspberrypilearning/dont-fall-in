## Cwis cyflym

Ateba'r tri chwestiwn. Mae awgrymiadau ar gael i dy arwain at yr ateb cywir.

Ar ôl i ti ateb pob cwestiwn, clicia ar **Gwirio fy ateb**.

Mwynha!

--- question ---

---
legend: Cwestiwn 1 o 3
---

![Y Llwyfan mewn gêm neidio lafa. Mae'r cymeriad ar y llwyfan diwedd, drws euraidd.](images/quiz-lava-stage.png)

Rwyt ti'n ennill y gêm hon drwy gyrraedd y drws aur, ac yn colli os byddi di'n glanio yn y pwll lafa. Dydy'r gêm ddim yn gweithio. Sut allet ti ei thrwsio?

```blocks3
when flag clicked
go to (Start v)
broadcast (start v)
```

```blocks3
when I receive [start v]
forever
if <touching color (#fff700) ?> then // gwirio colli
broadcast (stopio v) // rhwystro corluniau eraill
play sound (Lose v) until done
stop [all v]
end
if <touching color (#ff0000) ?> then // gwirio ennill
broadcast (stopio v) // rhwystro corluniau eraill
play sound (Win v) until done
stop [all v]
end
```


--- choices ---

- ( ) Newidi y lliw yn yr amod 'gwirio colli'

  --- adborth ---

Agos. Does gan yr amod 'gwirio colli' ddim y lliw cywir, ond fydd newid dim ond hyn ddim yn gwneud i'r gêm weithio.

  --- /adborth ---

- ( ) Newid y lliw yn yr amod 'gwirio ennill'

  --- feedback ---

Agos. Does gan yr amod 'gwirio ennill' ddim y lliw cywir, ond fydd newid dim ond hyn ddim yn gwneud i'r gêm weithio.

  --- /feedback ---

- (x) Cyfnewidiwch y lliwiau yn yr amodau 'gwirio ennill' a 'gwirio colli'

  --- feedback ---

Cywir. Mae'r lliwiau yn yr amodau 'gwirio colli' a 'gwirio ennill' yn y drefn anghywir! Bydd y chwaraewr yn ennill pan fydd yn disgyn yn y lafa ac yn colli pan fydd yn cyrraedd y drws aur! Bydd cyfnewid yr amodau yn trwsio hyn.

  --- /feedback ---

--- /choices ---

--- /question ---
