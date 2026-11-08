# informação

> Autor: **Rafael Moreira Xavier**
>
> Categoria: ForenseFácil

### Introdução

O desafio **informação**, disponibilizado pelo CYLAB, consiste em analisar uma imagem em busca de informações ocultas em seus metadados.

O objetivo é identificar possíveis dados inseridos no arquivo que não são visíveis ao visualizar a imagem normalmente e utilizá-los para encontrar a flag.

### Análise Inicial

O enunciado do desafio é:

> Os arquivos sempre podem ser alterados de forma secreta. Você consegue encontrar a bandeira?

O arquivo disponibilizado foi `cat.jpg`, uma imagem que, à primeira vista, não apresentava nenhuma informação suspeita.

[cat.jpg](https://challenge-files.cylabacademy.net/library/c585b4adbdaa06f409db7bf5012c2e58e9aab24669764a5f1cf0f9ce0d60dcfd/cat.jpg)

A partir do enunciado, percebi que seria necessário investigar informações que poderiam estar armazenadas internamente no arquivo, especialmente seus metadados.

### Interpretação

Para realizar a análise, utilizei o **Aperi'Solve**, uma ferramenta online que permite examinar arquivos de imagem e identificar informações que podem estar ocultas em sua estrutura.

Durante a análise, observei os metadados apresentados pela ferramenta e identifiquei um campo relacionado à licença (*License*).

Esse campo chamou minha atenção, pois seu conteúdo não parecia ser uma informação convencional de identificação da imagem. A partir disso, suspeitei que pudesse existir algum conteúdo codificado em seu valor.

[![Captura-de-tela-2026-11-08-184951.png](https://i.postimg.cc/j2kptPqj/Captura-de-tela-2026-11-08-184951.png)](https://postimg.cc/64njh7vs)

### Resolução

Com o conteúdo do campo *License* identificado, utilizei o **CyberChef** para investigar o possível formato da informação.

Na ferramenta, selecionei a operação **Magic**, que permite identificar automaticamente possíveis codificações e transformações aplicadas a um determinado conteúdo.

Ao inserir o valor encontrado nos metadados, o CyberChef identificou a codificação **Base64** e realizou a conversão para texto legível.

[![Captura-de-tela-2026-11-08-185229.png](https://i.postimg.cc/htmkRXkJ/Captura-de-tela-2026-11-08-185229.png)](https://postimg.cc/Wd2WM1bj)

Após a decodificação, foi possível recuperar o conteúdo original e identificar a flag solicitada pelo desafio.

> **Flag:** `academy{the_m3tadata_1s_modified}`

### Conclusão

O desafio **informação** demonstra a importância da análise de metadados em atividades de Forense Digital.

A resolução consistiu em investigar a imagem utilizando o Aperi'Solve, identificar um campo suspeito relacionado à licença e utilizar o CyberChef para reconhecer e decodificar o conteúdo em Base64.

Dessa forma, o desafio reforça que arquivos podem armazenar informações que não são perceptíveis visualmente, tornando a análise de metadados uma etapa importante na investigação de possíveis dados ocultos.
