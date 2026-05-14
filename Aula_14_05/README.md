# Gianluca Berria  
# Gabriel Santana  
# Emmanuel Avelino  

# RELATÓRIO DE IMPLEMENTAÇÃO DE INTERATIVIDADE, MODO ESCURO E EVENTOS EM JAVASCRIPT

## 1. Introdução

O presente relatório tem como objetivo descrever as implementações realizadas no projeto web, com destaque para a criação do modo escuro, a estilização dos elementos interativos e a aplicação de eventos de clique, hover e teclado.

As alterações foram desenvolvidas com foco na melhoria da experiência do usuário, na organização do código e na separação adequada entre estrutura, estilo e comportamento da página.

O projeto passou a utilizar um arquivo JavaScript externo, responsável por controlar a alternância entre modo claro e modo escuro, enquanto o arquivo CSS permaneceu encarregado da aparência visual da página.

---

## 2. Metodologia

A implementação foi realizada a partir da análise da estrutura HTML, do arquivo CSS já existente e da necessidade de adicionar comportamento dinâmico à interface.

Inicialmente, foi criado um botão com o identificador `darkModeToggle`, responsável por permitir ao usuário alternar entre os temas claro e escuro da página.

Em seguida, foi criado um arquivo JavaScript externo, chamado `script.js`, com o objetivo de concentrar a lógica de interação da página em um arquivo separado do HTML.

A chamada do arquivo JavaScript foi realizada no HTML por meio da tag:

```html
<script src="script.js" defer></script>

O uso do atributo defer permite que o navegador carregue o JavaScript sem bloquear o carregamento da página, garantindo também que os elementos HTML já estejam disponíveis quando o script for executado.

3. Implementações realizadas
3.1 Criação do botão de alternância de tema

Foi implementado um botão responsável por alternar entre o modo claro e o modo escuro da página:

<button id="darkModeToggle">🌙 Modo Escuro</button>

Esse botão funciona como o principal elemento de interação entre o usuário e o sistema de temas da página.

No modo claro, o botão indica a possibilidade de ativar o modo escuro.
No modo escuro, o texto do botão é alterado para indicar a possibilidade de retornar ao modo claro.

3.2 Implementação do evento de clique

A principal funcionalidade interativa foi construída com o evento de clique em JavaScript.

Foi utilizado o método addEventListener, que permite associar uma ação específica ao botão quando ele é pressionado pelo usuário.

const darkModeToggle = document.getElementById("darkModeToggle");

darkModeToggle.addEventListener("click", function () {
    document.body.classList.toggle("dark-mode");

    if (document.body.classList.contains("dark-mode")) {
        darkModeToggle.textContent = "☀️ Modo Claro";
    } else {
        darkModeToggle.textContent = "🌙 Modo Escuro";
    }
});

Ao clicar no botão, a classe dark-mode é adicionada ou removida do elemento body.

Quando essa classe está presente, o CSS aplica as cores do modo escuro.
Quando ela é removida, a página retorna ao modo claro.

Essa implementação torna o código mais organizado, pois o JavaScript apenas controla a classe aplicada, enquanto o CSS define a aparência visual de cada modo.

3.3 Implementação de hover

Também foram utilizados efeitos de hover no CSS para melhorar a resposta visual dos elementos interativos.

O hover permite que um elemento mude sua aparência quando o usuário posiciona o mouse sobre ele.

No botão de modo escuro, o efeito foi aplicado da seguinte forma:

#darkModeToggle:hover {
    background-color: #222222;
}

Além do botão, outros elementos da página também utilizam hover, como links da navegação e cards de download.

Esses efeitos são importantes porque indicam visualmente ao usuário que determinado elemento pode ser clicado ou selecionado.

Dessa forma, a página se torna mais intuitiva e agradável de utilizar.

3.4 Implementação de evento de teclado

Além do clique com o mouse, foi implementado suporte à interação por teclado.

Essa melhoria permite que o usuário ative o botão utilizando teclas como Enter ou Espaço, tornando a página mais acessível.

darkModeToggle.addEventListener("keydown", function (event) {
    if (event.key === "Enter" || event.key === " ") {
        event.preventDefault();
        darkModeToggle.click();
    }
});

Com essa implementação, quando o botão estiver selecionado e o usuário pressionar Enter ou Espaço, o JavaScript executará a mesma ação do clique.

Essa prática melhora a acessibilidade da página, pois nem todos os usuários navegam exclusivamente com mouse.

3.5 Estilização do botão no modo claro

No modo claro, o botão recebeu fundo preto e texto branco, criando contraste com o restante da página.

body:not(.dark-mode) #darkModeToggle {
    background-color: #000000;
    color: #ffffff;
    border: 1px solid #000000;
}

body:not(.dark-mode) #darkModeToggle:hover {
    background-color: #222222;
}

Essa escolha melhora a visibilidade do botão no modo claro e destaca sua função dentro da interface.

3.6 Estilização do botão no modo escuro

No modo escuro, o botão pode receber cores invertidas para indicar claramente a mudança de estado da interface.

body.dark-mode #darkModeToggle {
    background-color: #ffffff;
    color: #000000;
    border: 1px solid #ffffff;
}

body.dark-mode #darkModeToggle:hover {
    background-color: #dddddd;
}

Com isso, o botão mantém bom contraste tanto no modo claro quanto no modo escuro.

4. Código final do arquivo script.js

O arquivo script.js ficou responsável por controlar os eventos de clique e teclado relacionados ao botão de alternância de tema.

const darkModeToggle = document.getElementById("darkModeToggle");

darkModeToggle.addEventListener("click", function () {
    document.body.classList.toggle("dark-mode");

    if (document.body.classList.contains("dark-mode")) {
        darkModeToggle.textContent = "☀️ Modo Claro";
    } else {
        darkModeToggle.textContent = "🌙 Modo Escuro";
    }
});

darkModeToggle.addEventListener("keydown", function (event) {
    if (event.key === "Enter" || event.key === " ") {
        event.preventDefault();
        darkModeToggle.click();
    }
});
5. Importância dos eventos implementados

A implementação dos eventos contribuiu diretamente para a usabilidade da página.

O evento de clique permite a interação principal do usuário com o botão de modo escuro.

O hover melhora a resposta visual da interface, mostrando que determinados elementos são interativos.

O evento de teclado melhora a acessibilidade, permitindo que usuários que navegam sem mouse também consigam utilizar a funcionalidade.

Essas três formas de interação tornam a página mais completa, funcional e próxima das boas práticas modernas de desenvolvimento web.

6. Conclusão

A implementação do modo escuro e dos eventos de interação trouxe melhorias importantes para o projeto.

A separação entre HTML, CSS e JavaScript deixou o código mais organizado e facilitou futuras manutenções.

O HTML ficou responsável pela estrutura da página, o CSS pela aparência visual e o JavaScript pelo comportamento dinâmico.

O destaque principal da implementação está nos eventos utilizados:

evento de clique;
evento de hover;
evento de teclado.

Esses recursos tornam a página mais interativa, acessível e agradável para o usuário.

Dessa forma, o projeto passou a apresentar uma interface mais moderna, organizada e funcional.

Referências

MDN Web Docs - addEventListener
. Acesso em: 14 maio 2026.

MDN Web Docs - :hover
. Acesso em: 14 maio 2026.

MDN Web Docs - KeyboardEvent
. Acesso em: 14 maio 2026.

ChatGPT - OpenAI
. Acesso em: 14 maio 2026.