## Examen rápido

Contesta las tres preguntas. Hay pistas para guiarte hacia la respuesta correcta.

Cuando hayas respondido a cada pregunta, haz clic en **Revisar mi respuesta**.

¡Qué te diviertas!

--- question ---

---
legend: Pregunta 1 de 3
---

![El Escenario de un juego de saltar la lava. El personaje está en la plataforma final, una puerta dorada.](images/quiz-lava-stage.png)

Ganas este juego al llegar a la puerta dorada y pierdes si aterrizas en el pozo de lava. El juego no funciona. ¿Cómo podrías arreglarlo?

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

- (x) Intercambiar los colores en las condiciones de 'comprueba si pierdes'

  --- feedback ---

Casi. La condición de 'comprueba si pierdes' no tiene el color correcto, pero solo cambiarlo no hará que el juego funcione.

  --- /feedback ---

- ( ) Cambiando el color en la condición 'comprueba si ganas'

  --- feedback ---

Casi. La condición de 'comprueba si ganas' no tiene el color correcto, pero solo cambiarlo no hará que el juego funcione.

  --- /feedback ---

- (x) Intercambiar los colores en las condiciones de 'comprueba si ganas' y 'comprueba si pierdes'

  --- feedback ---

Sí. ¡Las condiciones 'comprueba si pierdes' y 'comprueba si ganas' tienen los colores invertidos! ¡El jugador ganará cuando caiga en la lava y perderá cuando llegue a la puerta dorada! Intercambiar las condiciones solucionará esto.

  --- /feedback ---

--- /choices ---

--- /question ---
