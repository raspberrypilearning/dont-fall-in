## Monter sur des plateformes

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Eh bien c'est trop facile ! 

Dans cette étape, tu ajouteras des plateformes sur lesquelles atterrir. Jumping on them will stop your sprite falling in. 
</div>
<div>
![](images/riding-example.png){:width="300px"}
</div>
</div>

--- task ---

Crée un sprite **Plateforme 1** sur lequel atterrir.

Peins un costume pour ton sprite **Plateforme 1**.

**Astuce :** Si tu veux que ton sprite `rebondisse`{:class="block3motion"} sans que le costume ne semble changer de direction, tu auras besoin d'un costume symétrique ou définis le sens de rotation sur **Ne tourne pas**.

![Le menu pop-up de la propriété de direction dans le panneau Sprite avec l'icône ne pas tourner sélectionnée.](images/dont-rotate.png)

--- /task ---

--- task ---

Ajoute du code à ton sprite **Plateforme 1** pour le faire bouger.

Tu auras peut-être besoin que ton sprite **Plateforme 1** `s'oriente à`{:class="block3motion"} `0` pour te déplacer de haut en bas sur l'écran.

--- collapse ---

---
title: Faire bouger ta plateforme
---

```blocks3
when I receive [start v]
point in direction (0) // add this block for left to right games
forever
move (4) steps // try different numbers
if on edge, bounce
end
```

--- /collapse ---

--- /task ---

--- task ---

**Test :** Clique sur le drapeau vert et assure-toi que ta plateforme se déplace correctement.

--- /task ---

--- task ---

Duplique ton sprite **Plateforme 1** et nomme-le **Plateforme 2**.

**Choisir :** Si tu veux avoir 3 plateformes, duplique à nouveau le sprite **Plateforme 1** et nomme-le **Plateforme 3**.

[[[scratch3-duplicate-sprite]]]

Expérimente avec le nombre de pas et la taille du sprite pour rendre chaque plateforme plus facile ou plus difficile à sauter.

--- /task ---

Détecte `si`{:class="block3control"} ton sprite **personnage** a atterri sur un sprite **Plateforme** et est en sécurité, `sinon`{:class="block3control"} ton sprite **personnage** est tombé !

--- task ---

Ajoute du code à ton sprite **personnage** pour détecter `si une couleur est touchée`{:class="block3sensing"} sur les sprites **plateformes**.

**Choisir :** Si ta plateforme a plusieurs couleurs, choisis la couleur sur laquelle ton personnage doit atterrir. Tu voudras peut-être qu'ils tombent à l'intérieur s'ils ne sont que sur le bord !

--- collapse ---

---
title: Si tu touches la plateforme
---

```blocks3
when I receive [start v]
forever
if <(size) = (landed) > then // not in the air
if <touching color (#b89d2f) ?> then // at end
broadcast (stop v) // stop other sprites
stop [other scripts in sprite v]
go to (End v)
play sound (Win v) until done
stop [all v]
end
+ if <touching color (#762356) ?> then // choose a colour on your platform
if <touching (Platform 1 v)> then
go to (Platform 1 v)
end
if <touching (Platform 2 v)> then
go to (Platform 2 v)
end
if <touching (Platform 3 v)> then
go to (Platform 3 v)
end
else
end
end
end
```

--- /collapse ---

--- /task ---

--- task ---

**Test :** Clique sur le drapeau vert et assure-toi que ton sprite peut monter sur les plateformes.

--- /task ---

--- task ---

Ajoute du code à ton sprite **personnage** pour détecter `si`{:class="block3control"} `touche`{:class="block3sensing"} la couleur d'arrière-plan, alors termine le jeu.

--- collapse ---

---
title: Sinon touche l'arrière-plan
---

```blocks3
when I receive [start v]
forever
if <(size) = (landed)> then // not in the air
if <touching color (#b89d2f) ?> then // at end
broadcast (stop v) // stop other sprites
stop [other scripts in sprite v] 
go to (End v)
play sound (Win v) until done
stop [all v]
end
if <touching color (#762356) ?> then // choose a colour on your platform
if <touching (Platform 1 v)> then
go to (Platform 1 v)
end
if <touching (Platform 2 v)> then
go to (Platform 2 v)
end
if <touching (Platform 3 v)> then
go to (Platform 3 v)
end
else
+ if <touching color (#37ab37) ?> then // choose your backdrop colour
broadcast (stop v)
stop [other scripts in sprite v] // prevent jumping after losing
hide
play sound (lose v) until done // add a sound of your choice
stop [all v]
end
end
end
```

--- /collapse ---

--- /task ---

--- task ---

**Test :** Joue à ton jeu et essaye de rater une plateforme. Assure-toi d'entendre le son d'échec.

--- /task ---

--- task ---

Ajoute du code à tes sprites **Plateforme** pour les empêcher de bouger lorsque le sprite **personnage** atteint la plateforme **Fin** ou tombe dedans !

```blocks3
when I receive [stop v]
stop [other scripts in sprite v]
```

--- /task ---

--- task ---

**Test :** Rejoue et assure-toi que les plateformes s'arrêtent à la fin de la partie. Le jeu se termine lorsque tu atteins la plateforme **Fin** ou lorsque tu tombes dedans.

--- /task ---

--- task ---

**Déboguer :**

--- collapse ---

---
title: Le jeu se termine trop tôt
---

Assure-toi que les blocs `si`{:class="block3control"} sont dans le bon ordre à l'intérieur de ton bloc `répéter indéfiniment`{:class="block3control"}. Vérifie soigneusement par rapport à l'exemple de code.

Si tu vérifies que le **personnage** touche l'arrière-plan avant qu'il n'ait eu la chance d'atterrir sur une plateforme, alors ta partie pourrait se terminer injustement !

Assure-toi que tes blocs `si`{:class="block3control"} pour vérifier les conditions de jeu sont à l'intérieur d'un bloc `si`{:class="block3control"} qui vérifie que la taille du **personnage** est normale. C'est bien que ton sprite touche la couleur d'arrière-plan en sautant. Ce n'est un problème que s'ils atterrissent dans la crème, la lave, la boue radioactive ou tout autre danger que tu as choisi.

--- /collapse ---

--- collapse ---

---
title: Les plateformes ne s'arrêtent pas lorsque je gagne ou que je perds
---

Regarde tes sprites**Plateforme** `quand je reçois`{:class="block3events"} et vérifie que le message est `stop`{:class="block3events"}.

```blocks3
when I receive [stop v]
stop [other scripts in sprite v]
```
Vérifie que le bloc `envoyer à tous`{:class="block3events"} à l'intérieur des blocs gagne et perd `si`{:class="block3control"} est `stop`{:class="block3events"}.

```blocks3
broadcast (stop v)
```

--- /collapse ---

--- /task ---

--- save ---
