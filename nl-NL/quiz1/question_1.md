## Snelle quiz

Beantwoord de drie vragen. Je wordt naar het juiste antwoord geleid.

Klik na het beantwoorden van elke vraag op **Controleer mijn antwoord**.

Veel plezier!

--- question ---

---
legend: Vraag 1 van 3
---

![Het speelveld van een lava-springspel. Je hoofdpersoon bevindt zich op het eindplatform, een gouden deur.](images/quiz-lava-stage.png)

Je wint dit spel door de gouden deur te bereiken en verliest als je in de lavaput belandt. Het spel werkt niet. Hoe zou je het kunnen oplossen?

```blocks3
when flag clicked
go to (Start v)
broadcast (start v)
```

```blocks3
when I receive [start v]
forever
if <touching color (#fff700) ?> then // controleer op verliezen
broadcast (stop v) // stop andere sprites
play sound (Lose v) until done
stop [alle v]
end
if <touching color (#ff0000) ?> then // controleer op winnen
broadcast (stop v) // stop andere sprites
play sound (Win v) until done
stop [alle v]
end
```


--- choices ---

- ( ) Verander de kleur in de 'controleer verlies' voorwaarde

  --- feedback ---

Bijna. De 'controleer verlies'-conditie heeft niet de juiste kleur, maar als je alleen dat verandert werkt het spel nog niet.

  --- /feedback ---

- ( ) Verander de kleur in de 'controleer winnen' voorwaarde

  --- feedback ---

Bijna. De 'controleer winnen'-voorwaarde heeft niet de juiste kleur, maar als je alleen dat verandert, werkt het spel nog niet.

  --- /feedback ---

- (x) Wissel de kleuren om in de voorwaarden 'controleer winnen' en 'controleer verlies'

  --- feedback ---

Ja. De voorwaarden 'controleer verliezen' en 'controleer winnen' hebben de verkeerde kleur! De speler wint wanneer hij in de lava valt en verliest wanneer hij de gouden deur bereikt! Het verwisselen van de voorwaarden lost dit op.

  --- /feedback ---

--- /choices ---

--- /question ---
