## Winnaar

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In deze stap zul je detecteren dat de speler het **Einde**-platform bereikt om het spel te winnen. 
</div>
<div>
![](images/winner-aims.png){:width="300px"}
</div>
</div>

Je gaat een `herhaal`{:class="block3control"} lus toevoegen die controleert of je **hoofdpersoon** op platformniveau is, en `als`{:class="block3control"} dat zo is of je hoofdpersoon het **Einde**-platform heeft bereikt.

--- task ---

**Maak een keuze:** Voeg een winnaarsgeluid toe dat bij je hoofdpersoon past.

--- /task ---

--- task ---

Voeg code toe om te detecteren wanneer je hoofdpersoon het **Einde**-platform bereikt met `raak ik kleur`{:class="block3sensing"}.

--- collapse ---

---
title: Beëindig het spel bij het aanraken van een kleur
---

**Hoofdpersoon**:

```blocks3
when I receive [start v]
forever
if <(size) = (landed)> then // not in the air
if <touching color (#b89d2f) ?> then // at end
broadcast (stop v) // stop other sprites
stop [other scripts in sprite v] // stop jumping after win
go to (End v)
play sound (Win v) until done
stop [all v]
end
end
end
```

Het is een goed idee om met `zend signaal`{:class="block3events"} een 'stop'-bericht uit te zenden om andere sprites te laten weten dat het spel is afgelopen. Het `stop andere scripts in sprite`{:class="block3control"} blok stopt de lus die het personage laat springen.

--- /collapse ---

Je moet de kleur die wordt waargenomen instellen op de kleur van je **Einde**-platform.

[[[scratch3-set-block-input-colour-with-eyedropper]]]

**Tip:** Het is een goed idee om een `zend signaal`{:class="block3events"} `stop`{:class="block3events"}-bericht aan het einde van je spel uit te sturen, om andere sprites te laten stoppen, zodat deze sprite kan nog iets doen zoals bijvoorbeeld een geluid afspelen voor hij stopt.

--- /task ---

--- task ---

**Test:** Klik op de groene vlag en spring met je hoofdpersoon over het speelveld. Zorg ervoor dat je het winnende geluid hoort wanneer je het **Einde**-platform bereikt.

**Tip:** Het is erg belangrijk dat je jouw project test voordat je naar de volgende stap gaat en meer code toevoegt. Het is moeilijker om fouten te vinden en op te lossen als je meer code hebt toegevoegd.

--- /task ---


--- task ---

**Fouten oplossen:**

--- collapse ---

---
title: Mijn sprite gaat niet naar het midden van het Einde-platform
---

Je moet ervoor zorgen dat al je sprite-kostuums gecentreerd zijn in de Teken-editor.

Het `ga naar (andere sprite)`{:class="block3motion"} blok verplaatst een sprite zodanig dat het midden van deze sprite zich op dezelfde positie bevindt als het midden van de andere sprite. Als de middelpunten op verschillende plaatsen zijn, gaat je **hoofdpersoon** niet naar het midden van een platform.

--- /collapse ---

--- collapse ---

---
title: Het spel eindigt te vroeg
---

Controleer of je sprite de Einde-kleur niet raakt als hij niet op het **Einde**-platform staat — als je dezelfde kleur ergens anders in je project gebruikt, kan je personage te snel sterven.

--- /collapse ---

--- collapse ---

---
title: Het geluid wordt niet afgespeeld wanneer ik op het Einde-platform beland
---

Klik op je **hoofdpersoon**-sprite en vervolgens op het tabblad 'Geluiden'. Zorg ervoor dat je het Einde-geluid aan je sprite hebt toegevoegd. Klik op de **Spelen**-knop om te controleren of het geluid werkt op je computer.

Klik op het tabblad **Code** en controleer of het juiste geluid in het `start geluid`{:class="block3sound"}-blok zit dat wordt uitgevoerd wanneer de sprite het **Einde**-platform bereikt.

Zorg ervoor dat de kleur correct is in het `raak ik kleur`{:class="block3sensing"}-blok. Selecteer het opnieuw als je het niet zeker weet. Soms lijken kleuren op elkaar, maar zijn ze niet hetzelfde.

```blocks3
when I receive [start v]
forever
if < (size) = (landed) > then // not in the air
+if <touching color (#b89d2f) ?> then // at end
broadcast (stop v) // stop other sprites
go to (End v)
+play sound (Win v) until done
stop [all v]
end
end
end
```

--- /collapse ---

Als je een fout hebt die we hier niet hebben behandeld, laat het ons dan weten in de feedback. Als je de fout zelf hebt opgelost (goed gedaan!), laat het ons dan ook weten.

**Tip:** Als je vastzit, probeer dan je code (hardop) voor te lezen om er achter te komen dat de code doet wat je denkt hij moet doen. Misschien vind je op die manier zelf wel de fout.

--- /task ---

--- save ---
