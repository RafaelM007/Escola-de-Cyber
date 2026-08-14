# Localização Cirúrgica


> Autor: **Rafael Moreira Xavier**
>
> Categoria: OSINT
> 


### Introdução

O desafio **Localização Cirúrgica** consiste em descobrir a localização exata de onde uma determinada fotografia foi tirada. Apesar de o monumento presente na imagem ser facilmente reconhecível, o objetivo é encontrar o ponto específico onde o fotógrafo estava.

### Análise Inicial

O enunciado do desafio é:

> Um monumento conhecido mundialmente pode ser encontrado em segundos. O verdadeiro desafio é descobrir exatamente onde o fotógrafo estava por meio de uma combinação de três palavras.

> Formato: `FLAG{xxxx.xxxx.xxxx}`

A imagem fornecida pelo desafio apresenta o **Taj Mahal**, um monumento mundialmente conhecido e localizado na Índia.

[![imagem-(2).jpg](https://i.postimg.cc/zfgck4VP/imagem-(2).jpg)](https://postimg.cc/Mcz56P0y)

Como a identificação do monumento era relativamente simples, o principal objetivo passou a ser descobrir o ponto exato de onde a fotografia havia sido tirada.

### Interpretação

O formato da flag apresenta três grupos separados por pontos:

```text
FLAG{xxxx.xxxx.xxxx}
```

Além disso, o enunciado menciona explicitamente uma **combinação de três palavras**. A partir dessa informação, pesquisei por ferramentas que utilizam três palavras para representar localizações.

Durante a pesquisa, encontrei o **What3Words**, um serviço que divide o mundo em pequenas áreas e atribui a cada uma delas uma combinação única de três palavras.

Isso indicou que provavelmente deveríamos encontrar o ponto exato da fotografia e, posteriormente, descobrir as três palavras correspondentes àquela localização.

### Resolução

Primeiramente, utilizei o **Google Maps** para localizar o Taj Mahal e analisar a região ao redor do monumento.

Utilizando o recurso de visualização em primeira pessoa do Google Maps, explorei a área ao redor do Taj Mahal e comparei os diferentes pontos de vista com a fotografia fornecida pelo desafio.

Após analisar a posição do monumento, estruturas ao redor e a perspectiva da imagem, consegui encontrar o ponto que correspondia ao local onde a fotografia havia sido tirada.

Com o ponto identificado, utilizei o **What3Words** para descobrir a combinação de três palavras correspondente à localização.

O resultado encontrado foi:

[![imagem-2026-08-14-180658684.png](https://i.postimg.cc/7LngDNcx/imagem-2026-08-14-180658684.png)](https://postimg.cc/f3k3fYDF)

```text
///commuted.anyway.stutter
```

Como o formato corresponde ao solicitado pelo desafio, removemos as barras `///` e colocamos as três palavras dentro do formato da flag.

> **Flag:** `FLAG{commuted.anyway.stutter}`

### Conclusão

O desafio **Localização Cirúrgica** demonstra uma aplicação prática de **OSINT e geolocalização**, mostrando que a identificação de um local conhecido é apenas o primeiro passo.

A partir do formato da flag e da referência a três palavras, foi necessário pesquisar por uma ferramenta que utilizasse esse sistema, levando à descoberta do What3Words. Em seguida, a análise da fotografia e a exploração do Google Maps permitiram encontrar o ponto exato de onde a imagem havia sido capturada.

Dessa forma, o desafio reforça a importância de observar não apenas a imagem apresentada, mas também as informações presentes no próprio enunciado e no formato esperado da resposta.
