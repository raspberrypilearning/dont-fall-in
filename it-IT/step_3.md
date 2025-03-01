## Salta, saltella, rimbalza o scivola!

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In questa fase, programmerai il tuo personaggio in modo che salti dalla piattaforma iniziale a quella finale. 
</div>
<div>
![](images/jump-example.png){:width="300px"}
</div>
</div>

Farai saltare il tuo personaggio sul percorso. Non preoccuparti di cadere.

--- task ---

<kbd>Scegli:</kbd> Aggiungi un suono di salto adatto al tuo personaggio.

[[[generic-scratch3-sound-from-library]]]

Ora fai saltare il tuo personaggio attraverso il percorso premendo la barra spaziatrice <kbd></kbd> sulla tastiera o toccando lo Stage sullo schermo.

[[[scratch3-top-down-jumping]]]

--- /task ---

--- task ---

**Test:** Premi la barra spaziatrice <kbd></kbd> o lo Stage per far saltare il tuo personaggio lungo il percorso fino alla piattaforma **Arrivo**.

Modifica il codice finché il personaggio non attraversa lo Stage in tre o quattro salti.

--- /task ---

**Suggerimento:** È molto comune nei giochi avere un blocco `per sempre`{:class="block3control"} con istruzioni `se`{:class="block3control"} al suo interno per fare qualcosa quando si verificano condizioni importanti.

--- task ---

**Debug:**

--- collapse ---

---
title: Il mio sprite non va alla piattaforma iniziale quando clicco sulla bandiera verde
---

Controlla di avere uno script di configurazione sul tuo sprite del personaggio ****:


```blocks3
when flag clicked // setup
+go to (Start v)
set [landed v] to [0]
set size to (landed) %
+go to [front v] layer
show
broadcast (start v) // start other scripts
```

Controlla che il nome nel blocco `raggiungi`{:class="block3motion"} corrisponda al nome dello sprite **Partenza**.

Controlla di avere un blocco `vai in primo piano `{:class="block3looks"}. Il tuo sprite potrebbe finire sotto la piattaforma iniziale!

Assicurati di non aver nascosto lo sprite del tuo **personaggio**. Se necessario, aggiungi un blocco `mostra`{:class="block3looks"} allo script di configurazione.


--- /collapse ---

--- collapse ---

---
title: Il mio sprite non va al centro della piattaforma di partenza
---

Devi assicurarti che tutti i costumi degli sprite siano centrati nell'editor Paint.

Il blocco `raggiungi`{:class="block3motion"} `altro sprite`{:class="block3motion"} sposta uno sprite in modo che il suo centro sia nella stessa posizione del centro dell'altro sprite. Se i loro centri sono nel posto sbagliato, il tuo personaggio **** non andrà al centro delle piattaforme.

--- /collapse ---

--- collapse ---

---
title: Il mio sprite punta o salta nella direzione sbagliata!
---

Aggiungi un blocco `punta in direzione`{:class="block3motion"} allo script di configurazione del personaggio ****oppure modifica la direzione nel riquadro sprite. Potrebbe anche essere necessario modificare lo stile di rotazione ``{:class="block3motion"}. Potrebbe anche essere necessario ruotare il  **costume** del tuo sprite in modo che sia rivolto verso destra.

--- /collapse ---

--- collapse ---

---
title: Il mio sprite non salta la distanza giusta
---

Guarda lo script del tuo **personaggio** `quando ricevo (start)`{:class="block3events"}. Prova a cambiare il numero di passi nei blocchi di `movimento`{:class="block3motion"}, oppure il numero di ripetizioni nei blocchi `ripeti`{:class="block3control"}.

```blocks3
+move [5] steps
```

Ricorda, dovrai modificare i numeri per la parte in cui sale e per la parte in cui scende del salto.

--- /collapse ---

--- collapse ---

---
title: Il mio sprite non cresce e non si restringe correttamente quando salta
---

Assicurati di avere un blocco `invio messaggio (start)`{:class="block3events"} alla fine dello script del tuo personaggio **** `quando si clicca sulla bandierina`{:class="block3events"}.

Guarda lo script del tuo **personaggio** `quando ricevo (start)`{:class="block3events"}.

Assicurati che il blocco `modifica dimensione`{:class="block3looks"} nel secondo blocco `ripeti`{:class="block3events"} abbia un numero negativo per rendere lo sprite più piccolo, ad esempio `-3`.

--- /collapse ---

Se hai riscontrato un bug che non abbiamo trattato qui, faccelo sapere tramite feedback. Se hai risolto il bug da solo (ben fatto!), faccelo sapere.

**Suggerimento:** Se sei bloccato, prova a leggere il codice ad alta voce o nella tua mente per assicurarti che faccia quello che pensi. Potresti trovare il bug.

--- /task ---

--- save ----
