- Gianluca Berria
- Gabriel Santana
- Emmanuel Avelino

---

## 1. Introdução

Este relatório apresenta as implementações realizadas no projeto web, com foco na adição de interatividade por meio de HTML, CSS e JavaScript.

Foram implementados:

- alternância entre modo claro e modo escuro;
- botão interativo para troca de tema;
- evento de clique;
- efeito visual de hover;
- suporte a evento de teclado;
- alteração dinâmica do texto do botão.

O objetivo foi melhorar a usabilidade da página e organizar melhor a separação entre estrutura, estilo e comportamento.

---

## 2. Organização dos arquivos

O projeto foi organizado em três arquivos principais:

```text
projeto/
├── index.html
├── style.css
└── script.js
```

O HTML define a estrutura da página.  
O CSS define a aparência visual.  
O JavaScript controla a interação do usuário com o botão de tema.

---

## 3. Chamada do JavaScript

O arquivo JavaScript foi chamado no HTML com a tag `script`:

```html
<script src="script.js" defer></script>
```

O atributo `defer` foi utilizado para garantir que o script seja executado após o carregamento da estrutura HTML.

---

## 4. Botão de troca de tema

Foi criado um botão responsável por alternar entre modo claro e modo escuro:

```html
<button id="darkModeToggle">🌙 Modo Escuro</button>
```

Quando o modo escuro é ativado, o texto do botão muda para:

```text
☀️ Modo Claro
```

Assim, o botão sempre indica a próxima ação disponível ao usuário.

---

## 5. Evento de clique

A troca de tema foi feita com um evento de clique no botão.

```javascript
const darkModeToggle = document.getElementById("darkModeToggle");

darkModeToggle.addEventListener("click", function () {
    document.body.classList.toggle("dark-mode");

    if (document.body.classList.contains("dark-mode")) {
        darkModeToggle.textContent = "☀️ Modo Claro";
    } else {
        darkModeToggle.textContent = "🌙 Modo Escuro";
    }
});
```

Ao clicar, a classe `dark-mode` é adicionada ou removida do `body`, permitindo que o CSS altere as cores da página.

---

## 6. Efeito de hover

O hover foi aplicado no CSS para indicar visualmente que o botão é interativo.

```css
#darkModeToggle:hover {
    background-color: #222222;
}
```

Esse efeito ocorre quando o usuário passa o mouse sobre o botão.

---

## 7. Evento de teclado

Também foi adicionado suporte ao teclado, permitindo ativar o botão com `Enter` ou `Espaço`.

```javascript
darkModeToggle.addEventListener("keydown", function (event) {
    if (event.key === "Enter" || event.key === " ") {
        event.preventDefault();
        darkModeToggle.click();
    }
});
```

Essa implementação melhora a acessibilidade da página.

---

## 8. Estilização do botão

No modo claro, o botão recebeu fundo preto e texto branco:

```css
body:not(.dark-mode) #darkModeToggle {
    background-color: #000000;
    color: #ffffff;
    border: 1px solid #000000;
}

body:not(.dark-mode) #darkModeToggle:hover {
    background-color: #222222;
}
```

No modo escuro, o botão recebeu cores invertidas:

```css
body.dark-mode #darkModeToggle {
    background-color: #ffffff;
    color: #000000;
    border: 1px solid #ffffff;
}

body.dark-mode #darkModeToggle:hover {
    background-color: #dddddd;
}
```

Com isso, o botão mantém bom contraste nos dois temas.

---

## 9. Código final do script.js

```javascript
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
```

---

## 10. Uso do ChatGPT

Durante o desenvolvimento, o ChatGPT, ferramenta de inteligência artificial da OpenAI, foi utilizado como apoio técnico.

A ferramenta auxiliou na organização do código, na explicação dos eventos, na revisão da lógica do JavaScript e na estruturação deste relatório.

---

## 11. Conclusão

A implementação tornou a página mais interativa e acessível.

O evento de clique permitiu a troca entre modo claro e modo escuro.  
O hover melhorou a resposta visual da interface.  
O evento de teclado ampliou a acessibilidade da funcionalidade.

Além disso, a separação entre HTML, CSS e JavaScript deixou o projeto mais organizado e de mais fácil manutenção.

---

## Referências

MDN WEB DOCS. EventTarget: addEventListener(). Disponível em: https://developer.mozilla.org/pt-BR/docs/Web/API/EventTarget/addEventListener. Acesso em: 14 maio 2026.

MDN WEB DOCS. :hover. Disponível em: https://developer.mozilla.org/pt-BR/docs/Web/CSS/:hover. Acesso em: 14 maio 2026.

MDN WEB DOCS. KeyboardEvent. Disponível em: https://developer.mozilla.org/pt-BR/docs/Web/API/KeyboardEvent. Acesso em: 14 maio 2026.

OPENAI. ChatGPT. Disponível em: https://openai.com/pt-BR/chatgpt/. Acesso em: 14 maio 2026.
