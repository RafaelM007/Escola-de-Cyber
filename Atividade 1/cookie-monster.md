# Cookie Monster

> Autor: **Rafael Moreira Xavier**
>
> Categoria: Web Exploitation
>

### Introdução

O desafio **Cookie Monster** consiste em acessar um website e encontrar a flag por meio da análise e manipulação dos cookies utilizados pela aplicação.

* [Página do desafio](https://monster.discloud.app/)

### Análise Inicial

O enunciado do desafio é bastante direto:

> Acesse o site para obter a flag.

Ao acessar o link fornecido, somos direcionados para uma página web.

[![Página inicial do desafio](https://i.postimg.cc/7ZwJ3s2m/Captura-de-tela-2026-08-13-234017.png)](https://postimg.cc/w74BHkFm)

Apesar de o enunciado não fornecer muitas informações, o próprio nome **Cookie Monster** fornece uma pista importante sobre o possível caminho da resolução. Dessa forma, uma das primeiras informações a serem analisadas são os **cookies** utilizados pelo website.

Os cookies são pequenos dados armazenados pelo navegador e enviados ao servidor em determinadas requisições. Eles podem ser utilizados para armazenar informações relacionadas à sessão, preferências do usuário e, em aplicações vulneráveis, até mesmo informações relacionadas aos seus privilégios.

### Interpretação

A partir do nome do desafio e da página acessada, podemos levantar a hipótese de que alguma informação relevante para a obtenção da flag está armazenada em um cookie.

Para verificar isso, abrimos as ferramentas de desenvolvedor do navegador e acessamos a área de armazenamento, onde podemos visualizar os cookies utilizados pelo website.

Ao analisar os cookies, encontramos uma informação relacionada ao nível de acesso do usuário, indicando se ele possui ou não privilégios de administrador.

### Resolução

Entre os cookies encontrados, identificamos o valor relacionado ao campo `admin`. Inicialmente, seu valor estava definido como:

```text
nao
```

Como o valor estava diretamente relacionado ao nível de acesso, alteramos o cookie de:

```text
admin = nao
```

para:

```text
admin = sim
```

Após realizar a alteração, recarregamos a página para que o novo valor do cookie fosse enviado ao servidor.

O website passou então a reconhecer o usuário como administrador. Isso indica que a aplicação estava confiando diretamente no valor fornecido pelo cliente para determinar o nível de privilégio do usuário.

Com o novo nível de acesso, a aplicação revelou a flag:

[![Flag](https://i.postimg.cc/vm1Yff3v/imagem-2026-08-13-235642132.png)](https://postimg.cc/WDvcPFRD)

> **Flag:** `FLAG{C00K1E_M0NST3R_MUNCH}`

### Conclusão

O desafio demonstra de forma simples uma vulnerabilidade relacionada à **confiança em informações armazenadas no lado do cliente**.

Ao analisar os cookies, foi possível identificar um parâmetro responsável por indicar se o usuário possuía privilégios de administrador. Como a aplicação não realizou uma validação adequada dessa informação no servidor, foi possível alterar o valor de `admin` de `nao` para `sim` e obter privilégios administrativos.

A resolução reforça a importância de analisar cookies, parâmetros e outras informações fornecidas pelo cliente durante a exploração de aplicações web. Também demonstra por que informações relacionadas a **autorização e privilégios de acesso não devem ser confiadas diretamente ao cliente**.
