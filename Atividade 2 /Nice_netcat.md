# Nice netcat...

> Autor: **Rafael Moreira Xavier**
>
> Categoria: Misc

### Introdução

O desafio **Nice netcat...**, disponibilizado pelo CYLAB, consiste em estabelecer uma comunicação com um serviço remoto utilizando o Netcat e interpretar os dados retornados pelo servidor para encontrar a flag.

O principal objetivo é identificar o padrão dos valores recebidos e descobrir como convertê-los para texto legível.

### Análise Inicial

O enunciado do desafio é:

> There is a nice program that you can talk to by using this command in a shell: `$ nc chatelaine.cylabacademy.net 11840`, but it doesn't speak English..

A partir do enunciado, foi possível identificar que seria necessário utilizar o **Netcat (nc)** para estabelecer uma conexão com o servidor disponibilizado pelo desafio.

O próprio enunciado também indicava que o programa não se comunicava em inglês, sugerindo que a resposta seria apresentada em algum formato diferente de texto convencional.

### Interpretação

Primeiramente, executei o comando fornecido pelo enunciado:

```bash
nc chatelaine.cylabacademy.net 11840
```

Após estabelecer a conexão, o servidor retornou uma sequência de números em vez de uma mensagem escrita.
[![Captura-de-tela-2026-11-08-183803.png](https://i.postimg.cc/qgVNbhfh/Captura-de-tela-2026-11-08-183803.png)](https://postimg.cc/tnkR7g4p)

Ao observar os valores recebidos, lembrei da tabela **ASCII**, utilizada para representar caracteres por meio de valores numéricos.

Isso indicou que os números provavelmente correspondiam aos códigos ASCII dos caracteres que formavam a mensagem original.

### Resolução

Com a sequência numérica em mãos, utilizei um conversor de **ASCII para texto** para transformar os valores recebidos em caracteres legíveis.

Copiei os números apresentados pelo terminal e inseri no conversor, que realizou a conversão e revelou a mensagem escondida.
[![Captura-de-tela-2026-11-08-183552.png](https://i.postimg.cc/RZmRqq3M/Captura-de-tela-2026-11-08-183552.png)](https://postimg.cc/7fB7WHMc)

Após a conversão, foi possível visualizar a mensagem contendo a flag solicitada pelo desafio.

> **Flag:** `academy{g00d_k1tty!_n1c3_k1tty!_6d1e6}`

### Conclusão

O desafio **Nice netcat...** demonstra uma aplicação prática do uso do Netcat para estabelecer conexões com serviços remotos e da codificação ASCII para representar caracteres por meio de números.

A resolução consistiu em executar o comando disponibilizado, analisar a sequência numérica retornada pelo servidor e reconhecer que aqueles valores poderiam representar caracteres ASCII.

Com a utilização de um conversor, foi possível transformar os números em texto legível e recuperar a flag.

Dessa forma, o desafio reforça a importância de reconhecer padrões nos dados recebidos e conhecer ferramentas e conceitos básicos de comunicação em rede e codificação de caracteres.
