## Questionnaire rapide

Réponds aux trois questions. Il y a des indices pour te guider vers la bonne réponse.

Lorsque tu as répondu à chaque question, clique sur **Vérifier ma réponse**.

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
