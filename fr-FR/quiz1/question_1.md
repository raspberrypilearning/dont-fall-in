## Réflexion

Bravo, tu as créé un jeu et personnalisé le gameplay ! Tu as appris quelques façons utiles de combiner des blocs Scratch pour créer un jeu, notamment :
+ Utiliser des blocs` répéter indéfiniment`{:class="block3control"} avec des instructions `si` {:class="block3control"} pour détecter des **conditions **importantes dans votre jeu et prendre des mesures
+ Diffuser un message `démarrer`{:class="block3control"} après avoir configuré ton personnage, pour que tout soit prêt lorsque tu démarres le jeu
+ Diffuser un message `stop`{:class="block3control"} lorsque tu détectes une **condition ** de finde jeu telle que gagner ou perdre, afin que d'autres scripts puissent s'arrêter et que tu puisses jouer un son ou faire une animation avant `stop [tout]`{:class="block3control"}

Maintenant, il est temps de réfléchir - la réflexion est une partie importante de l'apprentissage, car elle aide à établir de nouvelles connexions dans ton cerveau.

Réponds aux trois questions ci-dessous pour réfléchir à ce que tu as appris.

Après chaque question, appuie sur Soumettre. Tu seras guidé vers la bonne réponse. Tu peux faire cette activité autant de fois que tu le souhaites.

Amuse-toi bien !

--- question ---

---
legend: Question 1 sur 3
---

![La scène d'un jeu de saut de lave. Le personnage est sur la plateforme de fin, une porte dorée.](images/quiz-lava-stage.png)

Tu gagnes ce jeu en atteignant la porte dorée et tu perds si tu atterris dans la fosse de lave. Le jeu ne fonctionne pas. Comment pourrais-tu résoudre ce problème ?

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

- ( ) Changer la couleur dans la condition "test perdu"

  --- feedback ---

Fermer. La condition "test perdu" n'a pas la bonne couleur, mais le simple fait de changer cela ne fera pas fonctionner le jeu.

  --- /feedback ---

- ( ) Changer la couleur dans la condition "test gagné"

  --- feedback ---

Fermer. La condition "test gagné" n'a pas la bonne couleur, mais le simple fait de changer cela ne fera pas fonctionner le jeu.

  --- /feedback ---

- (x) Échanger les couleurs dans les conditions "test gagné" et "test perdu"

  --- feedback ---

Oui. Les conditions "test perdu" et "test gagné" ont les couleurs inversées ! Le joueur gagnera lorsqu'il tombera dans la lave et perdra lorsqu'il atteindra la porte dorée ! Échanger les conditions résoudra ce problème.

  --- /feedback ---

--- /choices ---

--- /question ---
