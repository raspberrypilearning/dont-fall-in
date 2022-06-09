## Spring, huppel, stuiter of glijd!

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In deze stap codeer je jouw hoofdpersoon om van het begin naar het eindplatform te springen. 
</div>
<div>
![](images/jump-example.png){:width="300px"}
</div>
</div>

Je gaat je personage over het speelveld laten springen. Het is niet erg als je personage er al in valt.

--- task ---

**Maak een keuze:** Voeg een springgeluid toe dat bij je hoofdpersoon past.

[[[generic-scratch3-sound-from-library]]]

Laat je hoofdpersoon nu over het speelveld springen door op de <kbd>spatie</kbd>-balk op een toetsenbord te klikken of op een tablet op het speelveld te tikken.

[[[scratch3-top-down-jumping]]]

--- /task ---

--- task ---

**Test:** Klik op de <kbd>spatie</kbd>-balk of speelveld om je hoofdpersoon over het speelveld te laten springen naar het **Einde**-platform.

Pas je code aan totdat het personage in drie of vier sprongen over het speelveld springt.

--- /task ---

**Tip:** Het is heel gebruikelijk dat games een `herhaal`{:class="block3control"}-blok hebben met `als`{:class="block3control"}-statements erin om iets te doen wanneer belangrijke voorwaarden juist zijn.

--- task ---

**Fouten oplossen:**

--- collapse ---

---
title: Mijn sprite gaat niet naar het Start-platform als ik op de groene vlag klik
---

Controleer of je een setup-script hebt op je **hoofdpersoon** sprite:


```blocks3
when flag clicked // instellen
+go to (Start v)
set [geland v] to [0]
set size to (geland) %
+go to [front v] layer
show
broadcast (start v) // andere scripts starten
```

Controleer of de naam in het `ga naar`{:class="block3motion"}-blok overeenkomt met de naam van je **Start**-sprite.

Controleer of je een `ga naar laag voorgrond`{:class="block3looks"} blok hebt. Je sprite bevindt zich mogelijk onder het Start-platform!

Zorg ervoor dat je jouw **hoofdpersoon**-sprite niet hebt verborgen. Voeg indien nodig een `verschijn`{:class="block3looks"}-blok toe aan je installatiescript.


--- /collapse ---

--- collapse ---

---
title: Mijn sprite gaat niet naar het midden van het Start-platform
---

Je moet ervoor zorgen dat al je sprite-kostuums gecentreerd zijn in de Teken-editor.

Het `ga naar`{:class="block3motion"} `andere sprite`{:class="block3motion"} blok verplaatst een sprite zodanig dat het midden van deze sprite zich op dezelfde positie bevindt als het midden van de andere sprite. Als de middelpunten op verschillende plaatsen zijn, gaat je **-hoofdpersoon** niet naar het midden van een platform.

--- /collapse ---

--- collapse ---

---
title: Mijn sprite wijst of springt in de verkeerde richting!
---

Voeg een `-richt naar`{:class="block3motion"}-blok toe aan het installatiescript van je **hoofdpersoon** of verander de richting in het sprite-venster. Misschien moet je ook de `maak draaistijl`{:class="block3motion"} wijzigen. Misschien moet je ook het **uiterlijk** van je sprite draaien zodat het naar rechts wijst.

--- /collapse ---

--- collapse ---

---
title: Mijn sprite springt te ver of niet ver genoeg
---

Kijk goed naar je **hoofdpersoon**'s `wanneer ik signaal (spring) ontvang`{:class="block3events"}-script. Probeer het aantal stappen in de `neem x stappen`{:class="block3motion"} blokken, of het aantal herhalingen in de `herhaal`{:class="block3control"} blokken te veranderen.

```blocks3
+move [5] steps
```

Denk er aan dat je de getallen voor het omhoog en omlaag springen moet veranderen.

--- /collapse ---

--- collapse ---

---
title: Mijn hoofdpersoon groeit en krimpt niet op de juiste manier als hij springt
---

Zorg ervoor dat je een `zend signaal (start)`{:class="block3events"} blok hebt aan het einde van je **hoofdpersoon**'s `wanneer op de vlag wordt geklikt`{:class="block3events"} script.

Kijk goed naar je **hoofdpersoon**'s `wanneer ik signaal (start) ontvang`{:class="block3events"} script.

Zorg ervoor dat het `verander grootte met`{:class="block3looks"} blok in het tweede `herhaal`{:class="block3events"} blok een negatief getal heeft om de sprite kleiner te maken, zoals `-3`.

--- /collapse ---

Als je een fout hebt die we hier niet hebben behandeld, laat het ons dan weten in de feedback. Als je de fout zelf hebt opgelost (goed gedaan!), laat het ons dan ook weten.

**Tip:** Als je vastzit, probeer dan je code (hardop) voor te lezen om er achter te komen dat de code doet wat je denkt hij moet doen. Misschien vind je op die manier zelf wel de fout.

--- /task ---

--- save ----
