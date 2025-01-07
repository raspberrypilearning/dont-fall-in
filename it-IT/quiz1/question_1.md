## Quiz veloce

Rispondi alle tre domande. Alcuni suggerimenti ti aiuteranno a trovare la risposta corretta.

Dopo aver risposto a ciascuna domanda, fai clic su **Controlla la mia risposta**.

Divertiti!

--- question ---

---
legend: Domanda 1 di 3
---

![La fase di un gioco di salti nella lava. Il personaggio si trova sulla piattaforma finale, una porta dorata.](images/quiz-lava-stage.png)

Si vince la partita raggiungendo la porta dorata, si perde se si finisce nella fossa di lava. Il gioco non funziona. Come potresti aggiustarlo?

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

- ( ) Cambia il colore nella condizione 'seleziona perso'

  --- feedback ---

Chiudi. La condizione "seleziona perso" non ha il colore giusto, ma cambiarlo semplicemente non farà funzionare il gioco.

  --- /feedback ---

- ( ) Cambia il colore nella condizione 'seleziona vinto'

  --- feedback ---

Chiudi. La condizione "seleziona vinto" non ha il colore giusto, ma cambiarlo semplicemente non farà funzionare il gioco.

  --- /feedback ---

- (x) Scambia i colori nelle condizioni "seleziona vinto" e "seleziona perso"

  --- feedback ---

Sì. Le condizioni "seleziona perso" e "seleziona vinto" hanno i colori invertiti! Il giocatore vincerà quando cadrà nella lava e perderà quando raggiungerà la porta dorata! Il problema si risolverà invertendo le condizioni.

  --- /feedback ---

--- /choices ---

--- /question ---
