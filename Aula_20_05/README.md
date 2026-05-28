* Gianluca Berria
* Gabriel Santana
* Emmanuel Avelino

# Análise de semelhanças entre o projeto web e conceitos de frameworks front-end

## 1. Introdução

Este documento apresenta uma análise comparativa entre o código desenvolvido no projeto da pasta `Aula_14_05` e conceitos presentes em frameworks front-end modernos, especialmente React, Angular e Vue.js, que foram citados no material de aula sobre prototipagem ágil com frameworks front-end.

O objetivo desta análise não é afirmar que o projeto utilizou diretamente esses frameworks, pois o código foi desenvolvido com HTML, CSS e JavaScript puro. O objetivo é identificar traços, semelhanças e aproximações conceituais entre a implementação realizada e práticas comuns ensinadas nas documentações e tutoriais desses frameworks.

O projeto analisado apresenta uma página web com estrutura HTML, estilização em CSS e interatividade por JavaScript. Entre os principais elementos observados estão: navegação, tabelas de download, cards para sistemas operacionais, modo escuro, botão interativo, responsividade, efeitos visuais e separação entre estrutura, aparência e comportamento.

## 2. Relação com o material da aula

O material de aula aborda o uso de frameworks front-end modernos, especialmente React, Angular e Vue.js, com foco em prototipagem ágil, construção de interfaces, componentes dinâmicos e responsividade.

Mesmo sem utilizar diretamente nenhum desses frameworks, o projeto apresenta características que se aproximam da lógica ensinada no material. A página foi organizada em partes visuais reutilizáveis, recebeu interatividade por evento de clique, possui alteração dinâmica de estado visual e utiliza responsividade para adaptação da interface.

Esses pontos se conectam com a ideia central do material: construir interfaces web mais organizadas, interativas e fáceis de manter.

## 3. Semelhanças com React

### 3.1 Componentização visual

O React ensina que interfaces podem ser pensadas como pequenos blocos reutilizáveis chamados componentes. A documentação oficial afirma que um componente é uma parte da interface que possui sua própria lógica e aparência, podendo ser tão pequeno quanto um botão ou tão grande quanto uma página inteira.

No projeto, embora não existam componentes React reais, há uma organização visual que lembra essa forma de pensar. Elementos como o cabeçalho, a navegação, os cards de download, as tabelas, o botão de tema e o rodapé funcionam como blocos separados da interface.

O exemplo mais evidente está nos cards de download. Cada card representa um sistema operacional e segue uma mesma estrutura: título, descrição visual e estilo próprio. Essa repetição organizada se aproxima da ideia de um componente reutilizável.

Assim, a semelhança com React não está na sintaxe, mas na maneira de estruturar visualmente a interface em partes independentes.

### 3.2 Estado de interface

O React também trabalha com a noção de estado, isto é, informações que a interface precisa “lembrar” para mudar sua aparência ou comportamento. No projeto, o modo escuro funciona como um estado visual: a página pode estar em modo claro ou em modo escuro.

No arquivo `script.js`, o botão de tema altera a classe `dark-mode` no corpo da página. Quando essa classe está presente, o CSS aplica outro conjunto de cores e estilos. Isso lembra o funcionamento de um estado em React, no qual uma alteração de valor provoca mudança visual na interface.

A diferença é que, em React, isso normalmente seria feito com `useState`; no projeto, foi feito de maneira manual com `classList.toggle`.

### 3.3 Eventos de usuário

A documentação de React ensina que eventos são usados para responder a interações do usuário, como cliques, foco e envio de formulários. No projeto, essa lógica aparece no botão de troca de tema.

O código usa um evento de clique para executar uma ação quando o usuário interage com o botão. Conceitualmente, isso se aproxima da ideia de `onClick` em React, embora a sintaxe utilizada seja a do JavaScript puro.

Portanto, há um traço claro de interatividade orientada por eventos, conceito muito presente em React.

## 4. Semelhanças com Angular

### 4.1 Separação entre estrutura, estilo e comportamento

Angular trabalha com uma separação organizada entre template, lógica e estilo. Em um projeto Angular, a interface é normalmente definida em um template HTML, a lógica fica em um arquivo TypeScript e a estilização em um arquivo CSS.

O projeto analisado possui uma separação semelhante, ainda que mais simples. O `index.html` define a estrutura da página, o `style.css` define a aparência visual e o `script.js` controla a interação do botão de tema.

Essa divisão também está descrita no README do projeto, que afirma que o HTML define a estrutura, o CSS define a aparência e o JavaScript controla a interação do usuário com o botão de tema.

Assim, há uma aproximação conceitual com a organização usada em Angular, pois cada camada do projeto possui uma função própria.

### 4.2 Template e evento

A documentação de Angular explica que templates são baseados em HTML e recebem recursos adicionais, como data binding e event listening. O projeto não usa a sintaxe Angular, mas apresenta uma lógica parecida: há elementos HTML que recebem comportamento por meio de JavaScript.

O botão de modo escuro é um bom exemplo. Ele existe no HTML como elemento visual e recebe comportamento no JavaScript por meio de um evento de clique. Em Angular, algo semelhante poderia ser feito com `(click)="alternarTema()"`.

A semelhança está na relação entre interface e comportamento: uma ação do usuário no template provoca uma mudança na interface.

### 4.3 Binding de classe e estilo

Angular possui recursos para alterar classes e estilos dinamicamente. A documentação mostra que classes e estilos podem ser vinculados a dados do componente.

No projeto, a classe `dark-mode` é adicionada e removida dinamicamente do `body`. O CSS, por sua vez, contém regras específicas para `body.dark-mode`, alterando cores, fundos, bordas, links, tabelas, cards e botões.

Isso se aproxima da ideia de class binding: uma condição ou estado altera a classe aplicada, e essa classe muda a aparência da interface.

A diferença é que, em Angular, esse processo seria integrado ao template; no projeto, foi feito diretamente com JavaScript puro.

## 5. Semelhanças com Vue.js

### 5.1 Manipulação dinâmica de classes

Vue.js possui um recurso bastante característico chamado class binding. A documentação de Vue explica que é comum manipular dinamicamente a lista de classes de um elemento, e que o framework oferece recursos especiais para isso.

No projeto, a alternância do modo escuro é exatamente uma manipulação dinâmica de classe. O JavaScript adiciona ou remove `dark-mode`, e o CSS responde a essa mudança.

Essa é uma das semelhanças mais fortes do projeto com Vue.js. Em Vue, seria comum fazer algo parecido com `:class="{ 'dark-mode': ativo }"`. No projeto, a mesma ideia aparece manualmente com `classList.toggle("dark-mode")`.

### 5.2 Reatividade visual

Vue trabalha com a ideia de reatividade: quando um dado muda, a interface reflete essa mudança. No projeto, a mudança da classe `dark-mode` altera imediatamente a aparência da página.

Embora não exista sistema reativo real, o comportamento final se aproxima do conceito: uma ação altera um valor visual da página e a interface responde.

O modo escuro, portanto, pode ser interpretado como um traço conceitual de reatividade.

### 5.3 Melhoria progressiva da página

Vue também é conhecido por permitir adoção progressiva, isto é, pode ser usado para adicionar interatividade a páginas existentes sem exigir a reescrita completa da aplicação.

O projeto segue uma lógica parecida: há uma página HTML tradicional e uma camada pequena de JavaScript adiciona comportamento interativo. Essa forma de trabalhar se aproxima mais de Vue e Alpine.js do que de Angular, pois não exige uma estrutura grande de aplicação.

## 6. Semelhanças com Bootstrap

### 6.1 Cards

Bootstrap possui um componente chamado card, descrito como um contêiner flexível e extensível para diferentes tipos de conteúdo. No projeto, a seção de downloads possui elementos `.download-card`, que funcionam de maneira parecida.

Cada card possui borda, sombra, espaçamento interno, título, texto e efeito de hover. Essa estrutura lembra bastante o padrão visual de cards usado em frameworks e bibliotecas de UI.

A semelhança é forte porque o projeto não apenas usa caixas visuais, mas cria blocos consistentes e repetidos, exatamente como se esperaria de um componente de card.

### 6.2 Layout flexível

Bootstrap também usa bastante a lógica de containers, linhas, colunas e flexbox para organizar elementos. No projeto, a navegação e os cards utilizam `display: flex`, `gap`, `justify-content`, `align-items` e `flex-wrap`.

Essas escolhas demonstram uma organização semelhante à mentalidade de frameworks CSS: criar layouts flexíveis, adaptáveis e visualmente consistentes.

## 7. Semelhanças com Tailwind CSS

### 7.1 Design utilitário e responsivo

Tailwind CSS é um framework baseado em classes utilitárias, usado para construir rapidamente interfaces modernas. O projeto não usa classes Tailwind, mas apresenta uma preocupação parecida com organização visual rápida, responsividade, espaçamentos, bordas, sombras e transições.

A diferença é importante: Tailwind coloca esses estilos diretamente no HTML por meio de classes utilitárias, enquanto o projeto concentra os estilos no CSS.

Mesmo assim, há uma semelhança conceitual na preocupação com pequenos ajustes visuais reutilizáveis: espaçamento, cores, hover, bordas, sombras, responsividade e tema escuro.

### 7.2 Modo escuro

Tailwind possui suporte a dark mode por meio de variantes específicas. No projeto, o modo escuro foi feito manualmente usando a classe `dark-mode`.

Esse é um traço bastante claro de prática moderna de UI. A ideia é a mesma: aplicar estilos diferentes quando a interface está em modo escuro.

## 8. Semelhanças com Alpine.js

### 8.1 Interatividade leve

Alpine.js é uma biblioteca voltada para adicionar comportamento diretamente em páginas HTML com pouca estrutura. A documentação de Alpine mostra exemplos com `x-data`, `x-bind` e `x-on`, usados para controlar estado, atributos e eventos.

O projeto se aproxima bastante dessa filosofia. Ele não cria uma aplicação completa com build, rotas ou componentes complexos; apenas adiciona uma pequena camada de interatividade a uma página HTML.

O botão de modo escuro é o melhor exemplo. Em Alpine, isso poderia ser feito com um estado `dark` e um evento `x-on:click`. No projeto, foi feito com `addEventListener` e `classList.toggle`.

A semelhança com Alpine.js é forte porque ambos seguem a ideia de interatividade simples e direta.

* reset global com `*`;
* uso de `box-sizing: border-box`;
* layout com `flex`;
* cards com `.download-card`;
* hover em links e cards;
* sombras com `box-shadow`;
* bordas arredondadas com `border-radius`;
* modo escuro com `body.dark-mode`;
* responsividade com `@media`;

Esses recursos aproximam o projeto de práticas comuns em Bootstrap, Tailwind, Material UI e frameworks modernos de front-end.

## 9. Conclusão

O projeto não utiliza diretamente React, Angular, Vue.js, Bootstrap, Tailwind, Alpine.js, jQuery. Entretanto, ele apresenta diversos traços conceituais desses frameworks e bibliotecas.

As semelhanças mais fortes são:

* com Vue.js, pela manipulação dinâmica de classes e resposta visual da interface;
* com Alpine.js, pela interatividade leve adicionada a uma página HTML tradicional;
* com Bootstrap, pelo uso de cards, responsividade e layout flexível;
* com React, pela organização visual em blocos e pela ideia de estado de interface;
* com Angular, pela separação entre estrutura, estilo e comportamento;
* com jQuery, pela seleção de elementos, evento de clique e alternância de classes;

Portanto, a análise mais adequada é afirmar que o projeto foi construído com tecnologias nativas da web, mas adota práticas e padrões visuais semelhantes aos encontrados em frameworks front-end modernos. Isso demonstra uma aproximação com a lógica de desenvolvimento usada nesses ecossistemas, ainda que sem dependência direta deles.

## Fontes consultadas

Material de aula: Desenvolvimento Web — Frameworks Front-end: Prototipagem Ágil com React, Angular e Vue.js.

https://react.dev/reference/react

https://angular.dev/overview

https://vuejs.org/guide/introduction.html

https://getbootstrap.com/docs/5.3/getting-started/introduction/

https://tailwindcss.com/docs/installation/using-vite

https://alpinejs.dev/start-here
