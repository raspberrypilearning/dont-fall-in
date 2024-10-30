## Teste rápido

Responda às três perguntas. Existem dicas para guiá-lo para a resposta correta.

Após responder cada pergunta, clique em **Ver minha resposta**.

Divirta-se!

--- question ---

---
legend: Pergunta 1 de 3
---

![O palco de um jogo de salto na lava. O personagem está na plataforma final, uma porta dourada.](images/quiz-lava-stage.png)

Você ganha este jogo ao alcançar a porta dourada e perde se cair no poço de lava. O jogo não está funcionando. Como você poderia consertar isso?

```blocks3
when flag clicked
go to (Início v)
broadcast (início v)
```

```blocks3
when I receive [início v]
forever
if <touching color (#fff700) ?> then // verificar perder
broadcast (parar v) // pare outros sprites
play sound (Lose v) until done
stop [todos v]
end
if <touching color (#ff0000) ?> then // verifique a vitória
broadcast (stop v) // pare outros sprites
play sound (Win v) until done
stop [todos v]
end
```


--- choices ---

- ( ) Alterar a cor na condição ‘escolha perder’

  --- feedback ---

Fechar. A condição 'escolher e perder' não tem a cor certa, mas apenas mudar isso não fará o jogo funcionar.

  --- /feedback ---

- ( ) Alterar a cor na condição 'checar vitória'

  --- feedback ---

Fechar. A condição 'checar vitória' não tem a cor certa, mas apenas mudar isso não fará o jogo funcionar.

  --- /feedback ---

- (x) Trocar as cores nas condições 'checar vitória' e 'checar perder'

  --- feedback ---

Sim. As condições 'checar perder' e 'checar vitória' têm as cores ao contrário! O jogador vencerá quando cair na lava e perderá quando chegar à porta dourada! Trocar as condições ira resolver isso.

  --- /feedback ---

--- /choices ---

--- /question ---
