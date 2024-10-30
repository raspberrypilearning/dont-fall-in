## Pule, salte, quique ou deslize!

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Nesta etapa, você codificará seu personagem para pular das plataformas do início ao fim. 
</div>
<div>
![](images/jump-example.png){:width="300px"}
</div>
</div>

Você fará seu personagem pular pelo palco. Não se preocupe em cair ainda.

--- task ---

**Escolha:** Adicione um som de salto adequado ao seu personagem.

[[[generic-scratch3-sound-from-library]]]

Agora faça seu personagem pular pelo palco pressionando a barra de <kbd>espaço</kbd> em um teclado ou tocando no palco em um tablet.

[[[scratch3-top-down-jumping]]]

--- /task ---

--- task ---

**Teste:** Toque na barra de <kbd>espaço</kbd> ou no Palco para fazer seu personagem pular pelo Palco até a plataforma **Fim**.

Ajuste seu código até que o personagem salte pelo palco em três ou quatro saltos.

--- /task ---

**Dica:** é muito comum que os jogos tenham um bloco `para sempre`{:class="block3control"} com condições `se`{:class="block3control"} dentro dele para fazer algo quando condições importantes se tornarem verdadeiras.

--- task ---

**Depurar:**

--- collapse ---

---
title: Meu sprite não vai para a plataforma Iniciar quando clico na bandeira verde
---

Verifique se você tem um script de configuração em seu sprite **personagem**:


```blocks3
when flag clicked // configurar
+go to (Início v)
set [pousado v] to [0]
set size to (pousado) %
+go to [da frente v] layer
show
broadcast (início v) // iniciar outros scripts
```

Verifique se o nome no bloco `ir para`{:class="block3motion"} corresponde ao nome do seu sprite **Iniciar**.

Verifique se você tem um bloco `vá para a camada frontal`{:class="block3looks"}. Seu sprite pode estar abaixo da plataforma Iniciar!

Certifique-se de não ter escondido seu sprite **personagem**. Adicione um bloco `exibir`{:class="block3looks"} ao seu script de configuração, se necessário.


--- /collapse ---

--- collapse ---

---
title: Meu sprite não vai para o centro da plataforma Iniciar
---

Você precisa ter certeza de que todas as suas fantasias de sprite estão centralizadas no editor Paint.

O bloco `vá para`{:class="block3motion"} `outro sprite`{:class="block3motion"} move um sprite para que seu centro fique na mesma posição que o centro do outro sprite. Se os centros deles estiverem no lugar errado, então seu **personagem** não irá para o centro das plataformas.

--- /collapse ---

--- collapse ---

---
title: Meu sprite está apontando na direção errada!
---

Adicione um ponto `na direção`{:class="block3motion"} bloco ao script de configuração do **personagem** ou altere a direção no painel sprite. Você também pode precisar alterar o `estilo de rotação`{:class="block3motion"}. Você também pode precisar girar o **traje** do seu sprite para que ele fique voltado para a direita.

--- /collapse ---

--- collapse ---

---
title: Meu sprite não salta a distância certa
---

Veja o script **do seu personagem** `quando eu recebo (pulo)`{:class="block3events"} script. Tente alterar o número de etapas nos blocos `mova`{:class="block3motion"} ou o número de repetições nos blocos `repetir`{:class="block3control"}.

```blocks3
+move [5] steps
```

Lembre-se, você precisará alterar os números das partes para cima e para baixo do salto.

--- /collapse ---

--- collapse ---

---
title: Meu sprite não cresce e encolhe corretamente quando salta
---

Certifique-se de ter um bloco `broadcast (start)`{:class="block3events"} no final da bandeira `quando clicado` do seu **personagem**{:class="block3events"} script.

Olhe para o seu **personagem** `quando eu receber (iniciar)`{:class="block3events"} script.

Certifique-se de que o bloco `alterar tamanho`{:class="block3looks"} no segundo bloco `repita`{:class="block3events"} tenha um número negativo para tornar o sprite menor, como `-3`.

--- /collapse ---

Se você tiver um bug que não abordamos aqui, informe-nos nos comentários. Se você mesmo corrigiu o bug (muito bem!), informe-nos também.

**Dica:** Se você estiver travado, tente ler seu código em voz alta ou mentalmente para ter certeza de que ele diz o que você pensa. Você pode encontrar o bug.

--- /task ---

--- save ----
