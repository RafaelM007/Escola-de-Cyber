# Cookie Monster

> Autor: **Rafael Moreira Xavier**
>
> Categoria: Web Exploitation
>

### Introdução

O desafio **Cookie Monster** consiste em acessar um website e encontrar a flag por meio da análise e manipulação dos cookies utilizados pela aplicação.

* [Página do desafio](https://monster.discloud.app/)

### Análise Inicial

Ao acessar o link fornecido pelo desafio, somos direcionados para uma página web.

[![Página inicial do desafio](Atividade 1/Imagens/site_cookie_monster.png)]

Como o desafio possui o nome **Cookie Monster**, uma das primeiras possibilidades a serem investigadas são os cookies utilizados pelo website. Para analisá-los, podemos abrir as ferramentas de desenvolvedor do navegador utilizando `F12` e acessar a seção de armazenamento de cookies.

### Resolução

Na área de cookies, encontramos uma informação relacionada ao nível de acesso do usuário.

[![Cookies do website](CAMINHO_DO_PRINT)](LINK_DO_PRINT)

Entre os cookies encontrados, identificamos um cujo valor poderia ser alterado para:

```text
admin
```

Após realizar a alteração e recarregar a página, o website passou a reconhecer o usuário como administrador.

[![Cookie alterado](CAMINHO_DO_PRINT)](LINK_DO_PRINT)

Com o novo nível de acesso, a aplicação revelou a flag.

[![Flag](CAMINHO_DO_PRINT)](LINK_DO_PRINT)

> **Flag:** `COLOCAR_FLAG_AQUI`

### Conclusão

O desafio demonstra uma vulnerabilidade relacionada à confiança em informações armazenadas no lado do cliente. Ao modificar o valor de um cookie responsável por indicar o nível de acesso, foi possível obter privilégios de administrador e acessar a flag.

A resolução também reforça a importância de analisar os cookies e outras informações armazenadas pelo navegador durante a exploração de aplicações web.
