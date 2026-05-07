Gianluca Berria

RELATÓRIO DE ANÁLISE DE CONFORMIDADE HTML5

1. Introdução

O presente relatório tem como objetivo apresentar uma análise da conformidade de uma página web com as diretrizes do HTML5. Para isso, foram realizados testes de validação utilizando a ferramenta W3C Markup Validation Service, disponível em validator.w3.org, cuja finalidade é verificar a marcação de documentos HTML, XHTML e outros formatos web.

A análise tomou como base as recomendações e especificações do HTML Living Standard, mantido pelo WHATWG, documento que descreve os elementos, atributos, regras de estruturação e padrões atuais da linguagem HTML.



2. Metodologia

A metodologia adotada consistiu na submissão do código HTML da página ao validador W3C Markup Validation Service. A ferramenta permite validar documentos por endereço URL, upload de arquivo ou inserção direta do código-fonte, apontando erros, avisos e inconformidades estruturais.

Após a validação inicial, os erros e avisos foram interpretados com apoio técnico do ChatGPT, ferramenta de inteligência artificial conversacional desenvolvida pela OpenAI para responder perguntas, auxiliar na análise de problemas e propor correções textuais e técnicas.



3. Resultados da validação

Durante a verificação, foram identificadas inconformidades relacionadas ao uso de práticas antigas de marcação HTML. Entre os principais problemas observados estavam a utilização de declaração DOCTYPE antiga, ausência de indicação adequada do idioma do documento, uso de atributos obsoletos para formatação visual e erros de sintaxe em algumas tags.

Tais problemas indicam que o código original possuía características herdadas de versões anteriores do HTML, especialmente do HTML 4, não estando plenamente ajustado às práticas modernas previstas pelo HTML5. Conforme a especificação atual do WHATWG, o HTML moderno deve priorizar estrutura semântica, separação entre conteúdo e apresentação visual, além do uso adequado de elementos como header, nav, main e footer.



4. Correções realizadas

Com base nos resultados do validador, foram feitas correções na estrutura da página. A declaração antiga de documento foi substituída por <!DOCTYPE html>, adequada ao HTML5. Também foi adicionada a indicação de idioma principal por meio do atributo lang="pt-BR".

Foram removidos atributos obsoletos como align, border, cellpadding, cellspacing, valign e width, que eram usados diretamente em tabelas e células. Esses atributos foram evitados por representarem práticas antigas de formatação visual, atualmente mais adequadas ao uso de CSS.

Além disso, a estrutura da página foi reorganizada semanticamente. O menu de navegação foi colocado no topo da página por meio dos elementos header e nav, enquanto o conteúdo principal foi mantido dentro de main. A área de créditos e direitos autorais foi transferida para um elemento footer, tornando o documento semanticamente mais apropriado.



5. Conclusão

A partir dos testes realizados no W3C Markup Validation Service, conclui-se que o código original da página não estava plenamente de acordo com as diretrizes do HTML5, pois apresentava erros estruturais, ausência de declaração moderna de documento e diversos atributos obsoletos.

Após as correções, o documento passou a apresentar estrutura mais próxima das recomendações modernas, com uso de DOCTYPE adequado, declaração de idioma, melhor organização semântica e eliminação de práticas antigas de formatação diretamente no HTML.

Portanto, a validação demonstrou que o processo de adequação ao HTML5 não depende apenas de a página funcionar visualmente no navegador, mas também de sua marcação estar correta, semântica e compatível com os padrões atuais da web.



Referências

7-ZIP. Download. Disponível em: https://www.7-zip.org/download.html
. Acesso em: 6 maio 2026.

OPENAI. ChatGPT. Disponível em: https://openai.com/pt-BR/index/chatgpt/
. Acesso em: 7 maio 2026.

W3C. The W3C Markup Validation Service. Disponível em: https://validator.w3.org/
. Acesso em: 7 maio 2026.

WHATWG. HTML Living Standard. Disponível em: https://html.spec.whatwg.org/multipage/
. Acesso em: 7 maio 2026.