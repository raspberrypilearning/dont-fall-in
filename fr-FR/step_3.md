## Saute, bondis, rebondis ou glisse !

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Dans cette étape, tu vas coder ton personnage pour qu'il saute des plateformes du début à la fin. 
</div>
<div>
![](images/jump-example.png){:width="300px"}
</div>
</div>

Tu vas faire sauter ton personnage à travers la scène. Ne t'inquiéte pas encore de tomber.

--- task ---

**Choisir :** Ajoute un son de saut adapté à ton personnage.

[[[generic-scratch3-sound-from-library]]]

Maintenant, fais sauter ton personnage à travers la scène en appuyant sur la barre <kbd>espace</kbd> sur un clavier ou en appuyant sur la scène sur une tablette.

[[[scratch3-top-down-jumping]]]

--- /task ---

--- task ---

**Test :** Appuie sur la barre <kbd>espace</kbd> ou sur la scène pour faire sauter ton personnage à travers la scène jusqu'à la plateforme **Fin**.

Ajuste ton code jusqu'à ce que le personnage saute à travers la scène en trois ou quatre sauts.

--- /task ---

**Astuce :** Il est très courant que les jeux aient un bloc `répéter indéfiniment`{:class="block3control"} avec des instructions `si` {:class="block3control"} à l'intérieur pour faire quelque chose lorsque des conditions importantes deviennent vraies.

--- task ---

**Déboguer :**

--- collapse ---

---
title: Mon sprite ne va pas sur la plateforme de démarrage lorsque je clique sur le drapeau vert
---

Vérifie que tu as un script de configuration sur ton sprite **personnage** :


```blocks3
when flag clicked // setup
+go to (Start v)
set [landed v] to [0]
set size to (landed) %
+go to [front v] layer
show
broadcast (start v) // start other scripts
```

Vérifie que ce nom dans le bloc `aller à`{:class="block3motion"} correspond au nom de ton sprite **Départ**.

Vérifie que tu disposes d'un bloc `aller à l'avant-plan`{:class="block3looks"}. Ton sprite pourrait être sous la plateforme "Départ" !

Assure-toi que tu n'as pas masqué ton sprite **personnage**. Ajoute un bloc `montrer`{:class="block3looks"} à ton script de configuration si nécessaire.


--- /collapse ---

--- collapse ---

---
title: Mon sprite ne va pas au centre de la plateforme "Départ"
---

Tu dois t'assurer que tous tes costumes de sprite sont centrés dans l'éditeur de peinture.

Les blocs `aller à`{:class="block3motion"} `autre sprite`{:class="block3motion"} déplace un sprite de sorte que son centre soit dans la même position que le centre de l'autre sprite. Si leurs centres sont au mauvais endroit, alors ton **personnage** n'ira pas au centre des plateformes.

--- /collapse ---

--- collapse ---

---
title: Mon sprite pointe ou saute dans la mauvaise direction !
---

Ajoute un bloc `s'orienter à`{:class="block3motion"} au script de configuration du **personnage** ou modifie la direction dans le volet sprite. Tu devras peut-être également modifier le `sens d'orientation`{:class="block3motion"}. Tu devras peut-être également faire pivoter le **costume** de ton sprite afin qu'il soit orienté vers la droite.

--- /collapse ---

--- collapse ---

---
title: Mon sprite ne saute pas à la bonne distance
---

Regarde le script de ton **personnage** `quand je reçois (saute)` {:class="block3events"}. Essaye de modifier le nombre de pas dans les blocs `avancer`{:class="block3motion"} ou le nombre de répétitions dans les blocs `répétitions`{:class="block3control"}.

```blocks3
+move [5] steps
```

N'oublie pas que tu devras modifier les nombres pour les parties montantes et descendantes du saut.

--- /collapse ---

--- collapse ---

---
title: Mon sprite ne grandit pas et ne rétrécit pas correctement lorsqu'il saute
---

Assure-toi d'avoir un bloc `envoyer à tous (départ)`{:class="block3events"} à la fin de ton script du **personnage**'s `quand le drapeau a cliqué`{:class="block3events"}.

Regarde le script de ton **personnage** `quand je reçois (départ)` {:class="block3events"}.

Assure-toi que le bloc `mettre à la taille`{:class="block3looks"} dans le deuxième bloc `répéter`{:class="block3events"} a un nombre négatif pour rendre le sprite plus petit tel que `-3`.

--- /collapse ---

Si tu as un bogue que nous n'avons pas traité ici, fais-le nous savoir dans les commentaires. Si tu as corrigé le bogue toi-même (bravo !), fais-le nous savoir également.

**Astuce :** Si tu es bloqué, essaye de lire ton code à haute voix ou dans ta tête pour t'assurer qu'il dit ce que tu penses qu'il fait. Tu pourrais trouver le bogue.

--- /task ---

--- save ----
