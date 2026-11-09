# Cookies

> Autor: **Rafael Moreira Xavier**
>
> Categoria: Web

### Introdução

O desafio **Cookies**, disponibilizado pelo CYLAB, consiste em explorar o funcionamento dos cookies utilizados por uma aplicação web para identificar diferentes conteúdos.

O objetivo é analisar os cookies armazenados pelo navegador, compreender como seus valores influenciam o comportamento da página e modificá-los para encontrar a flag.

### Análise Inicial

O enunciado do desafio é:

> Quem não gosta de biscoitos? Tente descobrir o melhor.

O desafio disponibiliza uma aplicação web. Ao acessar a página, encontrei um campo para pesquisar por um tipo de biscoito.
Inicialmente, inseri a palavra sugerida pela própria aplicação e recebi uma mensagem informando que aquele conteúdo era um cookie, mas não tinha nada de especial.

Essa resposta indicou que poderia existir alguma informação adicional sendo utilizada pela aplicação para determinar qual biscoito seria apresentado.

### Interpretação

Como o próprio nome do desafio é **Cookies**, decidi investigar os cookies armazenados pelo navegador.

Para isso, utilizei as ferramentas de desenvolvedor do navegador (Inspecionar), acessando a seção de armazenamento (*Application*) e, em seguida, a opção *Cookies*.

Durante a análise, percebi que existia um cookie chamado `name`, cujo valor era utilizado pela aplicação.

Ao modificar esse valor e atualizar a página, observei que a resposta apresentada mudava de acordo com o número informado.

Isso indicou que o servidor utilizava o valor do cookie para selecionar diferentes entradas, tornando possível testar valores numéricos até encontrar aquele que revelaria a flag.

### Resolução

Com essa descoberta, comecei a modificar manualmente o valor do cookie `name`, testando diferentes números e atualizando a página para observar as respostas.

Durante os testes, percebi que cada valor podia retornar um biscoito diferente ou uma resposta específica da aplicação.

Continuei alterando os valores até chegar ao número `18`.

Ao utilizar esse valor, a aplicação apresentou a flag, indicando que havia encontrado o conteúdo desejado.

[![Captura-de-tela-2026-11-08-210127.png](https://i.postimg.cc/bvSvZ76J/Captura-de-tela-2026-11-08-210127.png)](https://postimg.cc/67wKSmxJ)

> **Flag:** `academy{3v3ry1_l0v3s_c00k135_90a3a7cb}`

### Conclusão

O desafio **Cookies** demonstra como informações armazenadas no navegador podem influenciar diretamente o comportamento de uma aplicação web.

A resolução consistiu em identificar o cookie `name`, observar que seu valor numérico modificava o conteúdo apresentado pela página e testar diferentes possibilidades até encontrar o valor `18`, que revelou a flag.

Dessa forma, o desafio reforça a importância de compreender como os cookies funcionam e como a manipulação de valores controlados pelo cliente pode revelar falhas na lógica de uma aplicação web.
