## Kies je thema

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In deze stap voeg je een personage en achtergrond toe en maak je start- en eindplatforms. 
</div>
<div>
![](images/setup-example.png){:width="300px"}
</div>
</div>

--- task ---

Open een [nieuw Scratch-project](http://rpf.io/scratch-new){:target="_blank"} en verwijder de kattensprite. Scratch wordt in een nieuw browsertabblad geopend.

--- /task ---

--- task ---

Creëer een effen achtergrondkleur.

[[[scratch-paint-single-colour-backdrop]]]

--- /task ---

--- task ---

**Maak een keuze:** Beweegt je personage van links naar rechts of van onder naar boven?

![](images/direction-examples.png)

--- /task ---

--- task ---

Teken een nieuwe **Start**-platformsprite.

Begin met een eenvoudige vorm die een kleur heeft. You can turn the outline off by choosing the red diagonal line.

![](images/no-outline.png)

Je kunt later nog meer details toevoegen.

Centreer je kostuum in de Teken-editor.

[[[scratch-crosshair]]]

Plaats je **Start**-platformsprite waar je wilt dat je personage het spel start.

--- /task ---

--- task ---

Maak een eenvoudige **Einde**-platformsprite. Je kunt later meer details toevoegen.

Centreer je kostuum in de Teken-editor.

Plaats je **Einde**-platformsprite waar je wilt dat je personage het spel start.

--- /task ---

--- task ---

Selecteer de **hoofdpersoon**-sprite.

**Kies:** Wil je een **hoofdpersoon**-sprite toevoegen of er zelf een tekenen?

Misschien wil je een **hoofdpersoon**-sprite met bovenaanzicht toevoegen, zoals **Tatiana**, **Taylor** of **Trisha**.

![Afbeelding van de bovenaanzicht-sprites die in Scratch beschikbaar zijn](images/top-down-sprites.png)

Of teken je eigen **hoofdpersoon**-sprite. Begin met eenvoudige vormen en voeg later details toe. Centreer je kostuum in de Teken-editor.

[[[generic-scratch3-draw-sprite]]]

--- /task ---

--- task ---

Je **hoofdpersoon**-sprite heeft een startscript nodig om alles in te stellen voor het begin van het spel.

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

**Tip:** Het is een goed idee om een `zend signaal`{:class="block3events"} `start`{:class="block3events"}-bericht aan het einde van je installatiescript uit te sturen, om andere scripts te laten weten wanneer ze mogen beginnen, anders zouden ze kunnen beginnen voordat alles klaar is.

--- /task ---

--- task ---

**Fouten oplossen:**

--- collapse ---

---
title: Mijn sprite wijst in de verkeerde richting
---

De eigenschap **Richting** in het Sprite-paneel kan worden gebruikt om de richting te bepalen waarin de sprite wijst. Draai aan het wiel om een sprite in de gewenste richting te laten wijzen.

![Het sprite-venster met de richtingseigenschap geselecteerd. Er wordt een pop-upmenu weergegeven met een richtingswiel dat wordt gebruikt voor het aanpassen van de richting waarin de sprite wijst.](images/direction-property.png)

--- /collapse ---

--- /task ---

--- task ---

Geef je project een leuke titel waarin de beschrijving van je spel is opgenomen.

--- /task ---

--- save ---
