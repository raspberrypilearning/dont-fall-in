## Ganhador

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Nesta etapa, você detectará o jogador chegando à plataforma **Fim** para vencer o jogo. 
</div>
<div>
![](images/winner-aims.png){:width="300px"}
</div>
</div>

Você adicionará um laço `forever`{:class="block3control"} que verifica se seu **personagem** está no nível da plataforma e, em caso afirmativo, `se`{:class="block3control"} atingiu a plataforma **Fim**.

--- task ---

**Escolha:** Adicione um som vencedor ao seu personagem.

--- /task ---

###  End the game when touching a coloured platform

--- task ---

Use a `touching color`{:class="block3sensing"} block to detect when your character sprite reaches the **End** platform.


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

O bloco `parar outros scripts no sprite`{:class="block3control"} interrompe o laço que faz o personagem pular.

A `broadcast (stop v)`{:class="block3events"} message is used when your game is finished so that other sprites can stop, but this sprite can do something such as playing a sound before it stops.

--- /task ---

Use the eyedropper to pick the colour of your **End** platform

--- task ---

```blocks3
<touching color (#20f73b) ?>

```
Click on the colour input to open the colour picker and then click on the eyedropper at the bottom.

![](images/eye-dropper-tool.png)

Move the mouse pointer over to the End platform on the Stage and click to select the colour.

![](images/eye-dropper-stage.png)

The colour in the block input will change to match the colour you chose. Click in the Code area to close the colour picker.

--- /task ---

--- task ---

**Teste:** Clique na bandeira verde e pule seu personagem pelo palco. Certifique-se de ouvir o som vencedor quando chegar à plataforma **Fim**.

**Dica:** É muito importante que você teste seu projeto antes de passar para a próxima etapa e adicionar mais código. É mais difícil encontrar e corrigir bugs quando você adiciona mais código.

--- /task ---


--- task ---

**Depurar:**

--- collapse ---

---
título: Meu sprite não vai para o centro da plataforma Fim
---

Você precisa ter certeza de que todas as suas fantasias de sprite estão centralizadas no editor Paint.

O bloco `vá para (outro sprite)`{:class="block3motion"} outro sprite move um sprite para que seu centro fique na mesma posição que o centro do outro sprite. Se os centros deles estiverem no lugar errado, então seu **personagem** não irá para o centro das plataformas.

--- /collapse ---

--- collapse ---

---
título: O jogo termina muito cedo
---

Verifique se seu sprite não está tocando a cor final quando não estiver na plataforma **Fim** — se você usar a mesma cor em outro lugar do seu projeto, seu personagem poderá morrer muito cedo.

--- /collapse ---

--- collapse ---

---
título: O som não toca quando eu pouso na plataforma Fim
---

Clique no seu sprite **personagem** e depois na aba 'Sons'. Certifique-se de ter adicionado o som final ao seu sprite. Clique no botão **Jogar** para garantir que o som esteja funcionando no seu computador.

Clique na aba **Código** e verifique se o som correto está no bloco `tocar som`{:class="block3sound"} que é executado quando o sprite atinge a plataforma **Fim**.

Certifique-se de que a cor esteja correta no bloco `tocar cores`{:class="block3sensing"}. Selecione-o novamente se não tiver certeza. Às vezes, as cores parecem semelhantes, mas não são iguais.

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

Se você tiver um bug que não abordamos aqui, informe-nos nos comentários. Se você mesmo corrigiu o bug (muito bem!), informe-nos também.

**Dica:** Se você estiver travado, tente ler seu código em voz alta ou mentalmente para ter certeza de que ele diz o que você pensa. Você pode encontrar o bug.

--- /task ---

--- save ---
