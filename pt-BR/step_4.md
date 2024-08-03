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

--- task ---

Adicione código para detectar quando seu personagem atinge a plataforma **Fim** usando `tocando a cor`{:class="block3sensing"}.

--- collapse ---

---
título: Termine o jogo ao tocar na cor
---

**Personagem**:

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

É uma boa ideia `transmitir`{:class="block3events"} uma mensagem de 'parar' para que outros sprites saibam que o jogo terminou. O bloco `parar outros scripts no sprite`{:class="block3control"} interrompe o laço que faz o personagem pular.

--- /collapse ---

Você precisará definir a cor detectada para a cor da sua plataforma **Fim**.

[[[scratch3-set-block-input-colour-with-eyedropper]]]

**Dica:** É uma boa ideia `transmitir`{:class="block3events"} uma `parar`{: class="block3events"} quando você detecta que seu jogo terminou para que outros sprites possam parar, mas esse sprite pode fazer algo como reproduzir um som antes de parar.

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

Check that your sprite isn't touching the End colour when it's not on the **End** platform — if you use the same colour elsewhere in your project, then your character could die too soon.

--- /collapse ---

--- collapse ---

---
title: The sound doesn't play when I land on the End platform
---

Click on your **character** sprite and then the 'Sounds' tab. Make sure you have added the End sound to your sprite. Click on the **Play** button to make sure sound is working on your computer.

Click on the **Code** tab and check that the correct sound is in the `play sound`{:class="block3sound"} block that runs when the sprite reaches the **End** platform.

Make sure the colour is correct in the `touching colour`{:class="block3sensing"} block. Select it again if you're not sure. Sometimes colours look similar but aren't the same.

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

If you have a bug that we haven't covered here, then let us know in the feedback. If you fixed the bug yourself (well done!), let us know that too.

**Tip:** If you're stuck, try reading your code out loud or in your head to make sure it says what you think it does. You might find the bug.

--- /task ---

--- save ---
