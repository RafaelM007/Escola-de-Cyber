# Cebola Criptográfica

> Autor: **Rafael Moreira Xavier**
>
> Categoria: Cryptography
>

### Introdução

O desafio **Cebola Criptográfica** apresenta uma mensagem aparentemente composta apenas por números binários. O objetivo é identificar as diferentes camadas utilizadas para codificar a mensagem até chegar à flag.

### Análise Inicial

O enunciado do desafio é:

> À primeira vista, parece apenas linguagem de máquina bruta, mas nossos analistas acreditam que o remetente empacotou a mensagem em várias camadas para burlar nossos filtros.

A expressão **"várias camadas"** é uma pista importante para a resolução, indicando que provavelmente será necessário realizar mais de uma conversão para chegar à mensagem original.

Junto ao desafio, é disponibilizado um arquivo `.txt` contendo uma sequência de números binários.

Ao analisar o conteúdo do arquivo, podemos perceber que os valores estão organizados em grupos de números `0` e `1`, indicando que a primeira camada da mensagem está em **binário**.

### Interpretação

A partir do conteúdo do arquivo e da descrição do desafio, podemos concluir que não se trata simplesmente de uma mensagem escrita em binário. A referência às "várias camadas" indica que, após realizar uma conversão, o resultado provavelmente estará novamente codificado.

Para realizar essas conversões de maneira prática, utilizamos o **CyberChef**, uma ferramenta bastante utilizada para análise e transformação de dados.

### Resolução

Primeiramente, copiamos o conteúdo do arquivo `.txt` e utilizamos a ferramenta **Magic** do CyberChef.

O recurso **Magic** tenta identificar automaticamente possíveis codificações e transformações aplicáveis ao conteúdo fornecido.

A primeira transformação identificada foi a conversão de **binário para hexadecimal**. Após essa conversão, o resultado ainda não correspondia à flag, indicando que existia outra camada de codificação.

Em seguida, o resultado hexadecimal foi convertido, revelando uma nova sequência de caracteres.

A próxima camada identificada foi **Base64**. Após realizar a decodificação dessa camada, finalmente chegamos à mensagem contendo a flag.

[![imagem-2026-08-14-002749418.png](https://i.postimg.cc/ZRdD8KGr/imagem-2026-08-14-002749418.png)](https://postimg.cc/njnkZZcz)

> **Flag:** `FLAG{D1v3r54s_c4m4D45}`

### Conclusão

O desafio **Cebola Criptográfica** demonstra o conceito de **codificação em múltiplas camadas**, no qual uma informação é transformada diversas vezes antes de chegar ao seu conteúdo original.

Durante a resolução, foi necessário identificar que a sequência inicial estava em binário e, posteriormente, realizar as conversões de **binário → hexadecimal → Base64** até obter a flag.

O desafio também demonstra a utilidade de ferramentas como o **CyberChef**, que permitem identificar e realizar rapidamente diferentes transformações e codificações durante uma análise de CTF.
