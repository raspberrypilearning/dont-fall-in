## Scegli un tema

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In questa fase aggiungerai un personaggio e uno sfondo e creerai le piattaforme di partenza e di arrivo. 
</div>
<div>
![](images/setup-example.png){:width="300px"}
</div>
</div>

--- task ---

Apri un [nuovo progetto Scratch](http://rpf.io/scratch-new){:target="_blank"} ed elimina lo sprite del gatto. Scratch si aprirà in una nuova scheda del browser.

--- /task ---

--- task ---

Crea uno sfondo di colore uniforme.

[[[scratch-paint-single-colour-backdrop]]]

--- /task ---

--- task ---

**Scegli:** Il tuo personaggio si muoverà da sinistra verso destra o dal basso verso l'alto?

![](images/direction-examples.png)

--- /task ---

--- task ---

Dipingi un nuovo sprite della piattaforma **Partenza**.

Inizia con una semplice forma monocromatica. You can turn the outline off by choosing the red diagonal line.

![](images/no-outline.png)

Potrai aggiungere ulteriori dettagli in seguito.

Creare un nuovo costume nell'editor di Paint.

[[[scratch-crosshair]]]

Posiziona lo sprite della piattaforma **Partenza** nel punto in cui vuoi che il tuo personaggio inizi la partita.

--- /task ---

--- task ---

Crea uno sprite della piattaforma semplice **Arrivo**. Potrai aggiungere ulteriori dettagli in seguito.

Creare un nuovo costume nell'editor di Paint.

Posiziona il tuo sprite **Arrivo** sullo Stage in cui vuoi che il tuo personaggio termini il gioco.

--- /task ---

--- task ---

Crea uno sprite del **personaggio**.

**Scegli:** Vuoi aggiungere o dipingere uno sprite del **personaggio**?

Potresti voler aggiungere uno sprite **personaggio** visto dall'alto come **Tatiana**, **Taylor**, o **Trisha**.

![Immagine degli sprite dall'alto verso il basso disponibili in scratch](images/top-down-sprites.png)

Oppure dipingi il tuo sprite del **personaggio**. Inizia con forme semplici e aggiungi i dettagli in un secondo momento. Creare un nuovo costume nell'editor di Paint.

[[[generic-scratch3-draw-sprite]]]

--- /task ---

--- task ---

Lo sprite del tuo **personaggio** ha bisogno di uno script di avvio per preparare tutto all'inizio del gioco.

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

**Suggerimento:** è una buona idea `trasmettere`{:class="block3events"} un messaggio di `inizio`{:class="block3events"} alla fine dello script di installazione per far sapere agli altri script quando iniziare, altrimenti potrebbero avviarsi prima che tutto sia pronto.

--- /task ---

--- task ---

**Debug:**

--- collapse ---

---
title: Il mio sprite punta o salta nella direzione sbagliata
---

La proprietà **Direzione** nel riquadro Sprite può essere utilizzata per controllare la direzione in cui punta lo sprite. Gira la rotellina per far sì che uno sprite punti nella direzione desiderata.

![Il riquadro sprite con la proprietà direzione selezionata. Viene visualizzato un menu a comparsa con una rotellina direzionale utilizzata per regolare la direzione in cui punta lo sprite.](images/direction-property.png)

--- /collapse ---

--- /task ---

--- task ---

Assegna al tuo progetto un titolo che descriva il tuo gioco.

--- /task ---

--- save ---
