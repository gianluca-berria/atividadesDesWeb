# Gianluca Berria

# RELATÓRIO DE IMPLEMENTAÇÃO DO CSS RESPONSIVO

## 1. Introdução

O presente relatório tem como objetivo descrever a implementação do arquivo `style.css` desenvolvido para adequação visual e estrutural da página web conforme os princípios de design responsivo e boas práticas modernas de estilização com CSS.

A construção do estilo tomou como base as orientações presentes na documentação da [MDN Web Docs - Responsive Design](https://developer.mozilla.org/pt-BR/docs/Learn_web_development/Core/CSS_layout/Responsive_Design?utm_source=chatgpt.com), além das exigências descritas no documento PDF da atividade prática de Responsive Web Design.

Também foram utilizadas orientações técnicas fornecidas pelo [ChatGPT da OpenAI](https://openai.com/pt-BR/chatgpt/?utm_source=chatgpt.com) para análise estrutural, adaptação semântica e organização responsiva do layout.

---

## 2. Metodologia

A implementação do CSS foi realizada com foco na separação adequada entre estrutura HTML e apresentação visual, priorizando:

* organização semântica;
* adaptação do conteúdo a diferentes resoluções;
* utilização de unidades relativas;
* redução de overflow horizontal;
* melhoria da legibilidade;
* alinhamento com práticas modernas de desenvolvimento web.

Inicialmente foi analisada a estrutura HTML da página e posteriormente foram aplicadas estilizações globais para normalização visual utilizando reset CSS.

Após isso, foram implementados componentes específicos para:

* cabeçalho;
* barra de navegação;
* cartões de download;
* tabelas;
* listas;
* rodapé;
* comportamento responsivo em tablets e dispositivos móveis.

As alterações foram continuamente revisadas com apoio técnico do ChatGPT, utilizado como ferramenta auxiliar para validação lógica das decisões de implementação.

---

## 3. Implementações realizadas no style.css

### 3.1 Reset e configuração global

Foi aplicado um reset CSS utilizando o seletor universal `*` para remover margens e espaçamentos padrão dos navegadores, além da utilização de:

* `box-sizing: border-box`;
* `scroll-behavior: smooth`;
* padronização tipográfica;
* definição de largura total da página.

Essa abordagem melhora a previsibilidade do layout e evita inconsistências visuais entre navegadores.

---

### 3.2 Estruturação do layout

O layout principal foi organizado utilizando:

* `display: flex`;
* `flex-wrap`;
* `gap`;
* alinhamentos horizontais e verticais.

A navbar foi centralizada e preparada para reorganização automática em telas menores.

O conteúdo principal foi limitado em largura utilizando porcentagens relativas, permitindo adaptação proporcional ao tamanho da tela.

---

### 3.3 Implementação dos cards

Os cards de download foram desenvolvidos utilizando Flexbox para distribuição horizontal equilibrada.

Também foram adicionados:

* bordas arredondadas;
* sombras suaves;
* efeitos de hover;
* transições;
* diferenciação visual por sistema operacional.

Essas alterações melhoram a experiência visual e a identificação dos elementos interativos.

---

### 3.4 Tabelas responsivas

As tabelas receberam:

* largura total (`width: 100%`);
* `border-collapse`;
* padding interno;
* estilização alternada de linhas;
* controle de overflow horizontal.

A implementação buscou evitar quebra do layout em resoluções menores e aumentar a legibilidade das informações.

---

### 3.5 Responsividade e limitação para desktop

Foram utilizadas media queries para adaptação parcial do conteúdo em diferentes tamanhos de tela:

```css
@media (max-width: 1024px)
@media (max-width: 768px)
@media (max-width: 480px)
```

As principais alterações responsivas incluíram:

* reorganização vertical da navegação;
* empilhamento dos cards;
* ajuste de fontes;
* alteração de espaçamentos;
* expansão de elementos para largura total.

Entretanto, o projeto foi desenvolvido prioritariamente para ambiente desktop, considerando que o software 7-Zip é tradicionalmente utilizado em computadores e sistemas operacionais desktop.

Dessa forma, a responsividade aplicada teve como objetivo principal evitar quebras estruturais em resoluções menores, sem transformar a aplicação em uma experiência totalmente otimizada para dispositivos móveis.

A estratégia segue os princípios descritos na documentação da MDN sobre Responsive Design, especialmente no uso de layouts fluidos e adaptação progressiva.

---

## 4. Conclusão

A implementação do arquivo `style.css` permitiu modernizar a interface da página e adequá-la aos princípios contemporâneos de desenvolvimento responsivo.

O uso de Flexbox, media queries e unidades relativas tornou o layout mais flexível e funcional em diferentes resoluções, reduzindo problemas de alinhamento e overflow.

Além disso, a separação entre estrutura HTML e estilização visual contribuiu para uma organização mais adequada do projeto, facilitando futuras manutenções e melhorias.

Apesar da existência de adaptações responsivas, o foco principal do desenvolvimento permaneceu no ambiente desktop, devido ao público-alvo e à natureza do software apresentado na página.

---

## Referências

[MDN Web Docs - Responsive Design](https://developer.mozilla.org/pt-BR/docs/Learn_web_development/Core/CSS_layout/Responsive_Design?utm_source=chatgpt.com). Acesso em: 14 maio 2026.

[ChatGPT - OpenAI](https://openai.com/pt-BR/chatgpt/?utm_source=chatgpt.com). Acesso em: 14 maio 2026.

[7-Zip Official Website](https://www.7-zip.org/?utm_source=chatgpt.com). Acesso em: 14 maio 2026.
