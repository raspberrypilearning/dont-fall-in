## ¡Salta, brinca, rebota o deslízate!

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
En este paso programarás a tu personaje para saltar de una plataforma a otra. 
</div>
<div>
![](images/jump-example.png){:width="300px"}
</div>
</div>

Vas a hacer que tu personaje salte por el Escenario. No te preocupes todavía por caer.

--- task ---

**Elige:** Agrega un sonido de salto que se adapte a tu personaje.

[[[generic-scratch3-sound-from-library]]]

Ahora haz que tu personaje salte por el escenario presionando la barra <kbd>espacio</kbd> del teclado o tocando el Escenario en una tableta.

[[[scratch3-top-down-jumping]]]

--- /task ---

--- task ---

**Prueba:** Presiona la barra <kbd>espacio</kbd> o toca el Escenario para hacer que tu personaje salte por el Escenario hasta la plataforma **Fin**.

Ajusta tu código hasta que el personaje salte por el escenario en tres o cuatro saltos.

--- /task ---

**Sugerencia:** Es muy común que los juegos tengan un bloque `por siempre`{:class="block3control"} con sentencias `si`{:class="block3control"} dentro para hacer algo cuando condiciones importantes se vuelven verdaderas.

--- task ---

**Depurar:**

--- collapse ---

---
title: Mi objeto no va a la plataforma de Inicio cuando hago clic en la bandera verde
---

Comprueba que tengas un script de configuración en tu objeto **personaje**:


```blocks3
when flag clicked // configuración
+go to (Inicio v)
set [aterrizaje v] to [0]
set size to (aterrizaje) %
+go to [front v] layer
show
broadcast (comenzar v) // hace empezar otros scripts
```

Comprueba que el nombre en el bloque `ir a`{:class="block3motion"} coincida con el nombre de tu objeto **Inicio**.

Comprueba que tienes un bloque `ir a la capa de adelante`{:class="block3looks"}. ¡Tu objeto podría estar debajo de la plataforma de Inicio!

Asegúrate de no haber ocultado tu objeto **personaje**. Agrega un bloque `mostrar`{:class="block3looks"} a tu script si es necesario.


--- /collapse ---

--- collapse ---

---
title: Mi objeto no va al centro de la plataforma de Inicio
---

Tienes que asegurarte de que todos tus disfraces de objetos estén centrados en el Editor de dibujo.

El bloque `ir a`{:class="block3motion"} `otro objeto`{:class="block3motion"} mueve un objeto para que su centro esté en la misma posición que el centro del otro objeto. Si sus centros están en el lugar equivocado, entonces tu **personaje** no irá al centro de las plataformas.

--- /collapse ---

--- collapse ---

---
title: ¡Mi objeto mira o salta hacia la dirección equivocada!
---

Agrega un bloque `apuntar en dirección`{:class="block3motion"} al script de configuración de **personaje** o cambia la dirección en el panel de objetos. Es posible que también debas cambiar el `estilo de rotación`{:class="block3motion"}. También es posible que tengas que rotar el **disfraz** de tu objeto para que mire hacia la derecha.

--- /collapse ---

--- collapse ---

---
title: Mi objeto no salta la distancia correcta
---

Mira el script de tu **personaje** que dice `al recibir (salto)`{:class="block3events"}. Intenta cambiar el número de pasos en los bloques `mover`{:class="block3motion"} o el número de repeticiones en los bloques `repetir`{:class="block3control"}.

```blocks3
+move [5] steps
```

Recuerda que tendrás que cambiar el número para los saltos hacia arriba y los saltos hacia abajo.

--- /collapse ---

--- collapse ---

---
title: Mi sprite no crece ni se encoge correctamente cuando salta
---

Asegúrate de tener un bloque `enviar (comenzar)`{:class="block3events"} al final del script del **personaje** que dice `al presionar la bandera verde`{:class="block3events"}.

Mira el script de tu **personaje** que dice `al recibir (comenzar)`{:class="block3events"}.

Asegúrate de que el bloque `cambiar tamaño`{:class="block3looks"}, en el segundo bloque `repetir`{:class="block3events"} tenga un número negativo para hacer que el objeto sea más pequeño, como `-3`.

--- /collapse ---

Si tienes un error que no hemos incluido aquí, hazlo saber en los comentarios. Si solucionaste el error tú mismo (¡bien hecho!), háznoslo saber también.

**Sugerencia:** Si te atascaste, intenta leer tu código en voz alta o mentalmente para asegurarte de que dice lo que tú crees. Puede que encuentres el error.

--- /task ---

--- save ----
