## Gagnant

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Dans cette étape, tu détecteras le joueur atteignant la plateforme **Fin** pour gagner la partie. 
</div>
<div>
![](images/winner-aims.png){:width="300px"}
</div>
</div>

Tu vas ajouter une boucle `répéter indéfiniment`{:class="block3control"} qui vérifie si ton **personnage** est au niveau de la plateforme, et si oui, `si`{:class="block3control"} il a atteint la plateforme **Fin** .

--- task ---

**Choisir :** Ajoute un son de victoire à ton personnage.

--- /task ---

--- task ---

Ajoute du code pour détecter quand ton personnage atteint la plateforme **Fin** en utilisant `couleurs touche`{:class="block3sensing"}.

--- collapse ---

---
title: Terminer le jeu en touchant la couleur
---

**Personnage** :

```blocks3
when I receive [start v]
forever
if <(size) = (landed)> then // not in the air
if <touching color (#b89d2f) ?> then // at end
broadcast (stop v) // stop other sprites
stop [other scripts in sprite v] // stop jumping after win
go to (End v)
play sound (Win v) until done
stop [all v]
end
end
end
```

C'est une bonne idée d' `envoyer à tous`{:class="block3events"} un message "stop" pour faire savoir aux autres sprites que la partie est terminée. Le bloc `arrêter les autres scripts dans le sprite`{:class="block3control"} stoppe la boucle qui fait sauter le personnage.

--- /collapse ---

Tu devras définir la couleur détectée sur la couleur de ta plateforme **Fin**.

[[[scratch3-set-block-input-colour-with-eyedropper]]]

**Astuce :** C'est une bonne idée d' `envoyer à tous`{:class="block3events"} un message `stop`{:class="block3events"} lorsque tu détectes que ta partie est terminée afin que les autres sprites puissent s'arrêter, mais ce sprite peut faire quelque chose comme jouer un son avant qu'il ne s'arrête.

--- /task ---

--- task ---

**Test :** Clique sur le drapeau vert, puis fais sauter ton personnage à travers la scène. Assure-toi d'entendre le son de victoire lorsque tu atteins la plateforme **Fin**.

**Astuce :** Il est vraiment important que tu testes ton projet avant de passer à l'étape suivante et d'ajouter plus de code. Il est plus difficile de trouver et de corriger les bogues lorsque tu as ajouté plus de code.

--- /task ---


--- task ---

**Déboguer :**

--- collapse ---

---
title: Mon sprite ne va pas au centre de la plateforme "Fin"
---

Tu dois t'assurer que tous tes costumes de sprite sont centrés dans l'éditeur de peinture.

Le bloc `aller à (autre sprite)`{:class="block3motion"} déplace un sprite de sorte que son centre soit dans la même position que le centre de l'autre sprite. Si leurs centres sont au mauvais endroit, alors ton **personnage** n'ira pas au centre des plateformes.

--- /collapse ---

--- collapse ---

---
title: Le jeu se termine trop tôt
---

Vérifie que ton sprite ne touche pas la couleur "Fin" lorsqu'il n'est pas sur la plateforme **Fin**, si tu utilises la même couleur ailleurs dans ton projet, ton personnage pourrait mourir trop tôt.

--- /collapse ---

--- collapse ---

---
title: Le son ne joue pas lorsque j'atterris sur la plateforme "Fin"
---

Clique sur ton sprite **personnage** puis sur l'onglet "Sons". Assure-toi d'avoir ajouté le son de fin à ton sprite. Clique sur le bouton **Lecture** pour t'assurer que le son fonctionne sur ton ordinateur.

Clique sur l'onglet **Code** et vérifie que le bon son se trouve dans le bloc `jouer le son`{:class="block3sound"} qui s'exécute lorsque le sprite atteint la plateforme **Fin**.

Assure-toi que la couleur est correcte dans le bloc `couleur touchée`{:class="block3sensing"}. Sélectionne-le à nouveau si tu n'es pas sûr. Parfois, les couleurs se ressemblent mais ne sont pas identiques.

```blocks3
when I receive [start v]
forever
if < (size) = (landed) > then // not in the air
+if <touching color (#b89d2f) ?> then // at end
broadcast (stop v) // stop other sprites
go to (End v)
+play sound (Win v) until done
stop [all v]
end
end
end
```

--- /collapse ---

Si tu as un bogue que nous n'avons pas traité ici, fais-le nous savoir dans les commentaires. Si tu as corrigé le bogue toi-même (bravo !), fais-le nous savoir également.

**Astuce :** Si tu es bloqué, essaye de lire ton code à haute voix ou dans ta tête pour t'assurer qu'il dit ce que tu penses qu'il fait. Tu pourrais trouver le bogue.

--- /task ---

--- save ---
