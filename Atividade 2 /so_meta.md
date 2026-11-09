# So Meta

> Autor: **Rafael Moreira Xavier**
>
> Categoria: OSINT

### Introdução

O desafio **So Meta**, disponibilizado pelo CYLAB, consiste em analisar uma imagem para encontrar uma informação escondida em seus metadados.

O objetivo é investigar as propriedades internas do arquivo, identificando possíveis informações que não aparecem durante a visualização normal da imagem.

### Análise Inicial

O enunciado do desafio é:

> Find the flag in this picture.

O arquivo disponibilizado pelo desafio foi `pico_img.png`.

[pico_img.png](https://challenge-files.cylabacademy.net/library/8179732d3bcbaaf9dadfc7fe08aa5b7fbf1d3189b0a2dc90eca34dca38a85b4a/pico_img.png)

Como o nome do desafio é **So Meta**, percebi que a palavra poderia fazer referência aos metadados de arquivos. Isso indicou que a informação procurada provavelmente não estava visível diretamente na imagem, mas armazenada em alguma de suas propriedades.

### Interpretação

Para investigar o arquivo, utilizei o **Aperi'Solve**, uma ferramenta online que permite realizar diferentes análises em imagens, incluindo a identificação de metadados.

Durante a análise, observei as informações apresentadas pela ferramenta e identifiquei o campo **Artist**, que corresponde ao autor associado à imagem.

### Resolução

Primeiramente, carreguei o arquivo `pico_img.png` no Aperi'Solve e aguardei a conclusão da análise.

Em seguida, examinei os metadados apresentados pela ferramenta e localizei o campo **Artist**.

Diferentemente de um nome de autor convencional, o conteúdo desse campo apresentava diretamente a flag do desafio.

[![Captura-de-tela-2026-11-08-212426.png](https://i.postimg.cc/qMXr5kFG/Captura-de-tela-2026-11-08-212426.png)](https://postimg.cc/D8ZRWKnW)

Com isso, não foi necessário realizar nenhuma decodificação adicional, pois a flag já estava armazenada em texto legível nos metadados da imagem.

> **Flag:** `academy{s0_m3ta_45015e26}`

### Conclusão

O desafio **So Meta** demonstra a importância da análise de metadados em arquivos de imagem.

Dessa forma, o desafio reforça que imagens podem conter informações adicionais além de seu conteúdo visual, tornando a análise de metadados uma técnica importante em investigações de arquivos e atividades de CTF.
