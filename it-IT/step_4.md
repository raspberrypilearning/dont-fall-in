## Vittoria

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In questa fase, rileverai il giocatore che raggiunge la piattaforma **Fine** per vincere la partita. 
</div>
<div>
![](images/winner-aims.png){:width="300px"}
</div>
</div>

Aggiungerai un ciclo `per sempre`{:class="block3control"} che controlla se il tuo **personaggio** è a livello di piattaforma e, in tal caso, `se`{:class="block3control"} ha raggiunto la piattaforma **finale**.

--- task ---

**Scegli:** Aggiungi un suono di vittoria al tuo personaggio.

--- /task ---

###  Termina il gioco toccando una piattaforma colorata

--- task ---

Utilizza un blocco `sta toccando il colore`{:class="block3sensing"} per rilevare quando lo sprite del tuo personaggio raggiunge la piattaforma **Fine**.


```blocks3
when I receive [avvia v]
forever
if <(size) = (atterrato)> then // non in aria
if <touching color (#b89d2f) ?> then // alla fine
broadcast (stop v) // ferma altri sprite
stop [tutti gli altri script dello sprite v] // smetti di saltare dopo la vittoria
go to (End v)
play sound (Win v) until done
stop [tutto v]
end
end
end
```

Il blocco `interrompe gli altri script nello sprite`{:class="block3control"} interrompe il ciclo che fa saltare il personaggio.

Un messaggio `(stop v)`{:class="block3events"} viene utilizzato quando il gioco è terminato, in modo che gli altri sprite possano fermarsi, ma questo sprite può fare qualcosa come riprodurre un suono prima di fermarsi.

--- /task ---

Usa il contagocce per scegliere il colore della tua piattaforma **finale**

--- task ---

```blocks3
<touching color (#20f73b) ?>

```
Clicca sull'input dei colori per aprire il selettore del colore, poi clicca sul contagocce in basso.

![](images/eye-dropper-tool.png)

Sposta il puntatore del mouse sulla piattaforma Fine sullo Stage poi clicca per selezionare un colore.

![](images/eye-dropper-stage.png)

Il colore nell'input del blocco cambierà per corrispondere al colore scelto. Clicca nell'area del Codice per chiudere il contagocce.

--- /task ---

--- task ---

**Test:** Clicca sulla bandierina verde e muovi il mouse sullo stage. Assicurati di sentire il suono della vittoria quando raggiungi la piattaforma **Fine**.

**Suggerimento:** È molto importante testare il progetto prima di passare alla fase successiva e aggiungere altro codice. È più difficile trovare e correggere i bug quando si aggiunge altro codice.

--- /task ---


--- task ---

**Debug:**

--- collapse ---

---
title: Il mio sprite non va al centro della piattaforma finale
---

Devi assicurarti che tutti i costumi degli sprite siano centrati nell'editor Paint.

Il blocco `va ad (altro sprite)`{:class="block3motion"} sposta uno sprite in modo che il suo centro sia nella stessa posizione del centro dell'altro sprite. Se i loro centri sono nel posto sbagliato, il tuo **personaggio** non andrà al centro delle piattaforme.

--- /collapse ---

--- collapse ---

---
title: Il gioco finisce troppo presto
---

Controlla che il tuo sprite non tocchi il colore finale quando non si trova sulla piattaforma **finale**: se utilizzi lo stesso colore altrove nel tuo progetto, il tuo personaggio potrebbe morire troppo presto.

--- /collapse ---

--- collapse ---

---
title: Il suono non viene riprodotto quando atterro sulla piattaforma finale
---

Fai clic sullo sprite del tuo **personaggio** e poi sulla scheda "Suoni". Assicurati di aver aggiunto il suono della fine al tuo sprite. Fare clic sul pulsante **Riproduci** per assicurare che l'audio funzioni sul computer.

Fai clic sulla scheda **Codice** e controlla che il suono corretto sia nel blocco `riproduci suono`{:class="block3sound"} che viene eseguito quando lo sprite raggiunge la piattaforma **finale**.

Assicurati che il colore sia corretto nel blocco `colore di contatto`{:class="block3sensing"}. Selezionalo di nuovo se non sei sicuro. A volte i colori sembrano simili ma non sono uguali.

```blocks3
when I receive [avvia v]
forever
if < (size) = (atterrato) > then // non in aria
+if <touching color (#b89d2f) ?> then // alla fine
broadcast (stop v) // ferma altri sprite
go to (End v)
+play sound (Win v) until done
stop [tutto v]
end
end
end
```

--- /collapse ---

Se hai riscontrato un bug che non abbiamo trattato qui, faccelo sapere tramite feedback. Se hai risolto il bug da solo (ben fatto!), faccelo sapere.

**Suggerimento:** Se sei bloccato, prova a leggere il codice ad alta voce o nella tua mente per assicurarti che faccia quello che pensi. Potresti trovare il bug.

--- /task ---

--- save ---
