<!-- l10n-sync: source-file="workshop/04-design-vibes.md" -->
# Parte 4: Tematização orientada por design

---

Nesta parte, você vai usar os ciclos de planejamento e implementação do Copilot para projetar uma transformação completa do tema. Esta é uma abordagem de desenvolvimento orientada por design: comece com a visão, itere nos elementos visuais e deixe o Copilot cuidar do trabalho pesado de CSS.

## Tarefa 1: Planeje o tema retrô

<!-- track:vscode:start -->
Mude para **Plan** no GitHub Copilot Chat.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Use `/plan` no GitHub Copilot CLI ou pressione **Shift+Tab** até ativar o modo de planejamento.
<!-- track:cli:end -->

Insira este prompt:

> Quero transformar esta página em uma experiência completa de fliperama retrô. Planeje uma reformulação visual abrangente que inclua: efeitos de linhas de varredura CRT no fundo, brilho neon pulsante no título, selo VS animado com mudanças de cor em gradiente, sobreposição brilhante nas cartas de resultados dos usuários, animações de entrada flutuante nos campos, texto de carregamento alternando entre verde e roxo e efeitos de brilho ao passar o cursor sobre os quadrados de contribuições. Mantenha o fundo escuro (`#0a0a1a`) e use verde (`#5fed83`) e roxo (`#8a2be2`) como cores de destaque. Aplique um tema escuro com a fonte retrô Press Start 2P do Google Fonts.

O Copilot vai gerar um plano detalhado com todos os efeitos visuais. **Não aceite imediatamente** — revise o plano e itere:

- Sugira ajustes no tempo das animações (por exemplo, "Deixe o pulso neon mais lento, com cerca de 3 segundos").
- Pergunte sobre efeitos específicos (por exemplo, "Como vai funcionar a sobreposição brilhante nas cartas?").
- Peça mudanças na abordagem se algo não parecer adequado.

## Tarefa 2: Implemente o tema

Quando estiver satisfeito com o plano, peça ao Copilot para implementá-lo.

> Implemente o plano do tema de fliperama retrô que acabamos de criar.

O Copilot vai adicionar várias animações CSS, pseudoelementos e transições à sua folha de estilos. Isso pode incluir:

- `@keyframes` para linhas de varredura, pulso neon, brilho e efeitos de entrada flutuante.
- Pseudoelementos (`::before`, `::after`) para efeitos de sobreposição.
- Propriedades personalizadas do CSS para as cores do tema.
- Transições e estados de foco do cursor para elementos interativos.

<!-- track:cli:start -->
Depois que as alterações forem aplicadas, use `/diff` para revisar os estilos antes de aprová-los.
<!-- track:cli:end -->

## Tarefa 3: Ajuste o visual

> **⚠️ Não está vendo as alterações?** Se o novo tema ou as animações não aparecerem, pare o servidor de desenvolvimento (`Ctrl+C`), reinicie com `npm run dev` e atualize o navegador à força (`Ctrl+Shift+R`).

Mantenha a prévia no navegador aberta e itere no design. Experimente prompts como:

> O efeito de linhas de varredura está forte demais; reduza a opacidade para 0.03.

> Adicione uma cintilação elétrica sutil ao texto do título.

> O selo VS deve pulsar com mais intensidade.

Este é o **desenvolvimento orientado por design**: você está iterando no resultado visual em tempo real. Cada prompt refina a experiência até ficar do jeito que você quer. Não se contente com "bom o suficiente" — continue aprimorando até a página parecer parte de um fliperama.

## Tarefa 4: Atualize as instruções

Suas instruções devem refletir as principais decisões de design para manter os prompts seguintes alinhados.

<!-- track:vscode:start -->
Peça ao Copilot Chat:

> Adicione a `copilot-instructions.md` uma seção de guia de design que descreva o tema de fliperama retrô: cores, fontes e estilo das animações.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Peça ao Copilot CLI:

> Atualize as instruções do repositório com um guia breve de design para o tema de fliperama retrô: cores, fontes, estilo das animações e a regra de que novas interfaces devem manter a estética neon.
<!-- track:cli:end -->

Quando a página estiver como você quer, faça commit das instruções e das alterações de design.

## ✅ Parte 4 concluída

**O que você aprendeu:**

- Usar fluxos de planejamento para definir um **sistema de design antes da implementação**.
- **Iterar no resultado visual** com prompts de acompanhamento.
- **Atualizar as instruções após decisões importantes** para preservar a identidade visual.
