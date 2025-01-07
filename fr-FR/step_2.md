## Choisir ton thème

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Dans cette étape, tu vas ajouter un personnage et un arrière-plan, et créer des plateformes de début et de fin. 
</div>
<div>
![](images/setup-example.png){:width="300px"}
</div>
</div>

--- task ---

Ouvre un [nouveau projet Scratch](http://rpf.io/scratch-new){:target="_blank"} et supprime le sprite chat. Scratch s'ouvrira dans un autre onglet du navigateur.

--- /task ---

--- task ---

Crée un arrière-plan de couleur unie.

[[[scratch-paint-single-colour-backdrop]]]

--- /task ---

--- task ---

**Choisir :** Ton personnage se déplacera-t-il de gauche à droite ou de bas en haut ?

![](images/direction-examples.png)

--- /task ---

--- task ---

Peins un nouveau sprite de plateforme **Départ**.

Commence avec une forme simple d'une seule couleur. You can turn the outline off by choosing the red diagonal line.

![](images/no-outline.png)

Tu pourras ajouter plus de détails ultérieurement.

Centre ton costume dans l'éditeur de peinture.

[[[scratch-crosshair]]]

Positionne ton sprite de plateforme **Départ** à l'endroit où tu souhaites que ton personnage commence la partie.

--- /task ---

--- task ---

Crée un simple sprite de plateforme **Fin**. Tu pourras ajouter plus de détails ultérieurement.

Centre ton costume dans l'éditeur de peinture.

Positionne ton sprite **Fin** sur la scène où tu veux que ton personnage termine la partie.

--- /task ---

--- task ---

Crée un sprite **personnage**.

**Choisir :** Veux-tu ajouter ou peindre un sprite **personnage** ?

Tu voudras peut-être ajouter un sprite **personnage** en vue de dessus tel que **Tatiana**, **Taylor** ou **Trisha**.

![Image des sprites de haut en bas disponible dans Scratch](images/top-down-sprites.png)

Ou, peins ton propre sprite **personnage**. Commence avec des formes simples et ajoute des détails plus tard. Centre ton costume dans l'éditeur de peinture.

[[[generic-scratch3-draw-sprite]]]

--- /task ---

--- task ---

Ton sprite **personnage** a besoin d'un script de démarrage pour que tout soit configuré pour le début du jeu.

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

**Astuce :** C'est une bonne idée d' `envoyer à tous`{:class="block3events"} un message `départ`{:class="block3events"} à la fin de ton script de configuration pour indiquer aux autres scripts quand commencer, sinon ils pourraient commencer avant que tout ne soit prêt.

--- /task ---

--- task ---

**Déboguer :**

--- collapse ---

---
title: Mon sprite pointe dans la mauvaise direction
---

La propriété **Direction** dans le volet Sprite peut être utilisée pour contrôler la direction dans laquelle pointe le sprite. Tourne la roue pour faire pointer un sprite dans la direction dont tu as besoin.

![Le volet sprite avec la propriété direction sélectionnée. Un menu contextuel s'affiche avec une molette de direction utilisée pour ajuster la direction vers laquelle pointe le sprite.](images/direction-property.png)

--- /collapse ---

--- /task ---

--- task ---

Donne à ton projet un titre qui décrit ton jeu.

--- /task ---

--- save ---
