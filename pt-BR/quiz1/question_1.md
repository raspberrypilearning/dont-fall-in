## Teste rápido

Responda às três perguntas. Existem dicas para guiá-lo para a resposta correta.

Após responder cada pergunta, clique em **Ver minha resposta**.

Divirta-se!

--- pergunta ---

---
legenda: Pergunta 1 de 3
---

![O palco de um jogo de salto na lava. O personagem está na plataforma final, uma porta dourada.](images/quiz-lava-stage.png)

Você ganha este jogo ao alcançar a porta dourada e perde se cair no poço de lava. O jogo não está funcionando. Como você poderia consertar isso?

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


--- escolhas ---

- ( ) Alterar a cor na condição ‘escolha perder’

  --- comentários ---

Fechar. A condição 'escolher e perder' não tem a cor certa, mas apenas mudar isso não fará o jogo funcionar.

  --- /comentários ---

- () Alterar a cor na condição 'checar vitória'

  --- feedback ---

Fechar. A condição 'checar vitória' não tem a cor certa, mas apenas mudar isso não fará o jogo funcionar.

  --- /feedback ---

- (x) Trocar as cores nas condições 'checar vitória' e 'checar perder'

  --- feedback ---

Sim. As condições 'checar perder' e 'checar vitória' têm as cores ao contrário! O jogador vencerá quando cair na lava e perderá quando chegar à porta dourada! Trocar as condições ira resolver isso.

  --- /feedback ---

--- /choices ---

--- /questão ---
