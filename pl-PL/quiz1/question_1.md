## Szybki quiz

Odpowiedz na trzy pytania. Podpowiedzi naprowadzą Cię na właściwą odpowiedź.

Po udzieleniu odpowiedzi na każde pytanie kliknij przycisk **Sprawdź moją odpowiedź**.

Miłej zabawy!

--- question ---

---
legend: Pytanie 1 z 3
---

![Scena gry w skoki przez lawę. Postać znajduje się na końcowej platformie, przy złotych drzwiach.](images/quiz-lava-stage.png)

Wygrywasz tę grę docierając do złotych drzwi. Przegrywasz natomiast, jeśli wylądujesz w jeziorze pełnym lawy. Niestety, gra nie działa. Jak możesz to naprawić?

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

- ( ) Zmień kolor w warunku 'sprawdź przegraną'

  --- feedback ---

Blisko. Warunek 'sprawdź przegraną' nie ma odpowiedniego koloru, ale sama jego zmiana nie sprawi, że gra będzie działać.

  --- /feedback ---

- ( ) Zmień kolor w warunku 'sprawdź wygraną'

  --- feedback ---

Blisko. Warunek 'sprawdź wygraną' nie ma odpowiedniego koloru, ale sama jego zmiana nie sprawi, że gra będzie działać.

  --- /feedback ---

- (x) Zamień kolory w warunkach 'sprawdź wygraną' i 'sprawdź przegraną'

  --- feedback ---

Tak. Kolory warunków "sprawdź przegraną" i "sprawdź wygraną" są odwrócone! Gracz wygra, gdy wpadnie do lawy i przegra, gdy dotrze do złotych drzwi! Zamiana warunków rozwiąże ten problem.

  --- /feedback ---

--- /choices ---

--- /question ---
