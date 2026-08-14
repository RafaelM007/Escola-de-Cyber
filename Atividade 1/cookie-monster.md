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

[![Captura-de-tela-2026-08-13-234017.png](https://i.postimg.cc/7ZwJ3s2m/Captura-de-tela-2026-08-13-234017.png)](https://postimg.cc/w74BHkFm)

Como o desafio possui o nome **Cookie Monster**, uma das primeiras possibilidades a serem investigadas são os cookies utilizados pelo website. Para analisá-los, podemos abrir as ferramentas de desenvolvedor do navegador e acessar a seção de armazenamento de cookies.

### Resolução

Na área de cookies, encontramos uma informação relacionada ao nível de acesso do usuário. Com isso é possível alterar o valor de admin de *nao* para *sim*.  

Após realizar a alteração e recarregar a página, o website passou a reconhecer o usuário como administrador.
Com o novo nível de acesso, a aplicação revelou a flag.

[![imagem-2026-08-13-235642132.png](https://i.postimg.cc/vm1Yff3v/imagem-2026-08-13-235642132.png)](https://postimg.cc/WDvcPFRD)

> **Flag:** `FLAG{C00K1E_M0NST3R_MUNCH}`

### Conclusão

O desafio demonstra uma vulnerabilidade relacionada à confiança em informações armazenadas no lado do cliente. Ao modificar o valor de um cookie responsável por indicar o nível de acesso, foi possível obter privilégios de administrador e acessar a flag.

A resolução também reforça a importância de analisar os cookies e outras informações armazenadas pelo navegador durante a exploração de aplicações web.
