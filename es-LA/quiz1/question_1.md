## Reflexión

¡Bien hecho, creaste un juego y lo personalizaste! Aprendiste maneras útiles de combinar bloques de Scratch para crear un juego, que incluyen:
+ Usar bloques `por siempre`{:class="block3control"} con sentencias `si`{:class="block3control"} para detectar **condiciones** importantes en tu juego y pasar a la acción
+ Enviar un mensaje de `comenzar`{:class="block3control"} después de configurar tu personaje, para que todo esté listo cuando empieces el juego
+ Enviar un mensaje de `detener`{:class="block3control"} cuando detectas una ** condición ** de fin del juego, como ganar o perder, para que otros scripts puedan detenerse y puedas reproducir un sonido o hacer una animación antes de `detener [todos]`{:clase="bloque3control"}

Ahora es momento de reflexionar: esta es una parte importante del aprendizaje porque te ayuda a establecer nuevas conexiones en tu cerebro.

Responde las siguientes tres preguntas para reflexionar sobre lo que has aprendido.

Después de cada pregunta presiona enviar. Vamos a guiarte hacia la respuesta correcta. Puedes realizar esta actividad tantas veces como quieras.

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

- ( ) Cambiando el color en la condición 'comprueba si pierdes'

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
