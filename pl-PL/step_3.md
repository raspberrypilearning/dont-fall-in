## Skacz, podskakuj, odbijaj się lub szybuj!

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
W tym kroku zakodujesz swoją postać tak, aby przeskakiwała z platformy początkowej na końcową. 
</div>
<div>
![](images/jump-example.png){:width="300px"}
</div>
</div>

Sprawisz, że Twoja postać będzie skakać po scenie. Nie martw się jeszcze wpadaniem.

--- task ---

**Wybierz:** Dodaj dźwięk skoku pasujący do Twojej postaci.

[[[generic-scratch3-sound-from-library]]]

Teraz spraw, by Twoja postać przeskoczyła przez scenę, naciskając klawisz <kbd>spacja</kbd> na klawiaturze lub dotykając sceny, jeśli używasz tabletu.

[[[scratch3-top-down-jumping]]]

--- /task ---

--- task ---

**Test:** Naciśnij klawisz <kbd>spacja</kbd> lub dotknij Scenę, aby Twoja postać przeskoczyła przez Scenę na platformę **End**.

Dostosuj swój kod, aż postać przeskoczy scenę w trzech lub czterech skokach.

--- /task ---

**Wskazówka:** Bardzo często w grach występuje blok `zawsze`{:class="block3control"} zawierający instrukcje `jezeli`{:class="block3control"} w środku, które służą do wykonania określonej czynności, gdy spełnione zostaną ważne warunki.

--- task ---

**Debugowanie:**

--- collapse ---

---
title: Mój duszek nie przechodzi na platformę Start po kliknięciu zielonej flagi
---

Sprawdź, czy masz skrypt początkowy na duszku **postaci**:


```blocks3
when flag clicked // setup
+go to (Start v)
set [landed v] to [0]
set size to (landed) %
+go to [front v] layer
show
broadcast (start v) // start other scripts
```

Sprawdź, czy nazwa w bloku `idź do`{:class="block3motion"} odpowiada nazwie duszka **Start**.

Sprawdź, czy masz blok `przesuń na wierzch`” {:class="block3looks"}. Twój duszek może znajdować się pod platformą Start!

Upewnij się, że nie ukryłeś duszka **postaci**. Jeśli zajdzie taka potrzeba, dodaj blok `pokaż`{:class="block3looks"} do skryptu początkowego.


--- /collapse ---

--- collapse ---

---
title: Mój duszek nie trafia na środek platformy Start
---

Musisz się upewnić, że wszystkie kostiumy duszków są wyśrodkowane w edytorze Paint.

Blok `idź do`{:class="block3motion"} `innego duszka`{:class="block3motion"} przesuwa duszka tak, że jego środek znajduje się w tej samej pozycji, co środek drugiego duszka. Jeśli ich środki znajdują się w niewłaściwym miejscu, twoja **postać** nie trafi na środek platformy.

--- /collapse ---

--- collapse ---

---
title: Mój duszek wskazuje lub skacze w złym kierunku!
---

Dodaj blok `ustaw kierunek`{:class="block3motion"} do skryptu początkowego **postaci** lub zmień kierunek w panelu duszka. Może być także konieczna zmiana `stylu obrotu`{:class="block3motion"}. Być może będziesz musiał też obrócić **kostium** swojego duszka tak, aby był skierowany w prawo.

--- /collapse ---

--- collapse ---

---
title: Mój duszek nie skacze na odpowiednią odległość
---

Spójrz na blok **kiedy otrzymam (skok)**{:class="block3events"} w skrypcie swojego duszka`postaci`. Spróbuj zmienić liczbę kroków w blokach `idź`{:class="block3motion"} lub liczbę powtórzeń w blokach `powtórzeń`{:class="block3control"}.

```blocks3
+move [5] steps
```

Pamiętaj, że będziesz musiał zmienić wartości liczb dla skoku w górę i w dół.

--- /collapse ---

--- collapse ---

---
title: Mój duszek nie rośnie i nie kurczy się prawidłowo podczas skoku
---

Upewnij się, że masz `nadaj komunikat (start)`{:class="block3events"} na końcu skryptu **postaci**i `, gdy flaga jest kliknięta.`{:class="block3events"}.

Spójrz na blok **kiedy otrzymam (skok)**{:class="block3events"} w skrypcie swojego duszka `postaci`.

Upewnij się, że blok `zmień rozmiar`{:class="block3looks"} w drugim `powtórz`{:class="block3events"} ma liczbę ujemną, aby zmniejszyć duszka, na przykład `-3`.

--- /collapse ---

Jeśli masz błąd, którego tutaj nie omówiliśmy, daj nam znać w komentarzu. Jeśli sam naprawiłeś błąd (brawo!), daj nam znać.

**Wskazówka:** Jeśli utkniesz, spróbuj przeczytać kod na głos lub w myślach, aby upewnić się, że robi to, co myślisz. Być może wtedy znajdziesz błąd.

--- /task ---

--- save ----
