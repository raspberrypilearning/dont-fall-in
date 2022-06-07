## Reflectie

Goed gedaan, je hebt een spel gemaakt en de spelregels aangepast! Je hebt een aantal handige manieren geleerd om Scratch-blokken te combineren om een spel te maken, waaronder:
+ Het gebruik van `herhaal`{:class="block3control"} blokken met `als`{:class="block3control"} statements om belangrijke **voorwaarden** in je spel te detecteren en actie te ondernemen
+ Een `start`{:class="block3control"}-bericht uitzenden nadat je je personage hebt ingesteld, zodat alles klaar is wanneer je het spel start
+ Een `stop`{:class="block3control"} bericht uitzenden wanneer je een speleinde-**voorwaarde** zoals winnen of verliezen detecteert, zodat andere scripts kunnen stoppen en je een geluid kunt afspelen of een animatie kunt doen voor `stop [alle]`{:class="block3control"}

Nu is het tijd om te reflecteren - reflecteren is een belangrijk onderdeel van leren, omdat het helpt om nieuwe verbindingen in je hersenen te maken.

Beantwoord de drie onderstaande vragen om terug te kijken op wat je hebt geleerd.

Druk na elke vraag op Controleer mijn antwoord. Je wordt naar het juiste antwoord geleid. Je kunt dit zo vaak doen als je wilt.

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
