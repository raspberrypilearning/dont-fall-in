## Ganador

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
En este paso detectarás que jugador llegue a la plataforma **Fin** para ganar el juego. 
</div>
<div>
![](images/winner-aims.png){:width="300px"}
</div>
</div>

Agregarás un bucle `por siempre`{:class="block3control"} que verifica si tu **personaje** está al nivel de la plataforma y, si es así, `si`{:class="block3control"} ha alcanzado la plataforma **Fin**.

--- task ---

**Elige:** Agrega un sonido de victoria a tu personaje.

--- /task ---

--- task ---

Agrega código para detectar cuándo tu personaje llega a la plataforma **Fin** usando `tocando el color`{:class="block3sensing"}.

--- collapse ---

---
title: Termina el juego tocando el color
---

**Personaje**:

```blocks3
when I receive [comenzar v]
forever
if <(size) = (aterrizaje)> then // no está en el aire
if <touching color (#b89d2f) ?> then // en el final
broadcast (detener v) // en el final
stop [other scripts in sprite v] // deja de saltar cuando gana
go to (Fin v)
play sound (Win v) until done
stop [all v]
end
end
end
```

Es una buena idea `enviar`{:class="block3events"} un mensaje de 'detener' para que otros objetos sepan que el juego ha terminado. El bloque `detener otros programas en el objeto`{:class="block3control"} detiene el bucle que hace que el personaje salte.

--- /collapse ---

Tendrás que establecer que el color que se detecte sea el mismo color de tu plataforma **Fin**.

[[[scratch3-set-block-input-colour-with-eyedropper]]]

**Sugerencia:** Es una buena idea `enviar`{:class="block3events"} un mensaje de `detener`{:class="block3events"} cuando detectes que tu juego ha terminado para que otros objetos puedan detenerse, pero este objeto puede hacer algo, como reproducir un sonido antes de que se detenga.

--- /task ---

--- task ---

**Prueba:** Haz clic en la bandera verde y luego salta con tu personaje por el escenario. Asegúrate que escuches el sonido de victoria cuando llegues a la plataforma **Fin**.

**Sugerencia:** Es muy importante que pruebes tu proyecto antes de que pases al siguiente paso y agregues más código. Es más difícil encontrar y corregir errores cuando has agregado más código.

--- /task ---


--- task ---

**Depurar:**

--- collapse ---

---
title: Mi objeto no va al centro de la plataforma de Fin
---

Tienes que asegurarte de que todos tus disfraces de objetos estén centrados en el Editor de dibujo.

El bloque `ir a (otro objeto)`{:class="block3motion"} mueve un objeto para que su centro esté en la misma posición que el centro del otro objeto. Si sus centros están en el lugar equivocado, entonces tu **personaje** no irá al centro de las plataformas.

--- /collapse ---

--- collapse ---

---
title: El juego termina demasiado pronto
---

Verifica que tu objeto no esté tocando el color del Fin cuando no está en la plataforma **Fin**; si usas el mismo color en otra parte de tu proyecto, entonces tu personaje podría morir demasiado pronto.

--- /collapse ---

--- collapse ---

---
title: El sonido no se reproduce cuando aterrizo en la plataforma Fin
---

Haz clic en tu objeto **personaje** y luego en la pestaña 'Sonidos'. Asegúrate de haber agregado el sonido de Fin a tu objeto. Haz clic en el botón **Reproducir** para asegurarte de que el sonido funcione en tu computadora.

Haz clic en la pestaña **Código** y verifica que el sonido correcto esté en el bloque `tocar sonido`{:class="block3sound"} que se ejecuta cuando el objeto llega a la plataforma de **Fin**.

Asegúrate de que el color sea correcto en el bloque `tocando el color`{:class="block3sensing"}. Selecciónalo de nuevo si no estás seguro. A veces los colores se ven similares pero no son iguales.

```blocks3
when I receive [comenzar v]
forever
if < (size) = (aterrizaje) > then // no está en el aire
+if <touching color (#b89d2f) ?> then // en el final
broadcast (detener v) // en el final
go to (Fin v)
+play sound (Win v) until done
stop [all v]
end
end
end
```

--- /collapse ---

Si tienes un error que no hemos incluido aquí, hazlo saber en los comentarios. Si solucionaste el error tú mismo (¡bien hecho!), háznoslo saber también.

**Sugerencia:** Si te atascaste, intenta leer tu código en voz alta o mentalmente para asegurarte de que dice lo que tú crees. Puede que encuentres el error.

--- /task ---

--- save ---
