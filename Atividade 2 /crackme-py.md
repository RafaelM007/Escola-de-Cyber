# crackme-py

> Autor: **Rafael Moreira Xavier**
>
> Categoria: Reverse Engineering

### Introdução

O desafio **crackme-py**, disponibilizado pelo CYLAB, consiste em analisar um código-fonte escrito em Python para encontrar uma informação que está armazenada de forma codificada.

O objetivo é identificar como o programa realiza a decodificação e utilizar essa lógica para recuperar a flag.

### Análise Inicial

O desafio disponibiliza o arquivo `crackme_gen.py`, contendo o código-fonte que deve ser analisado.

[crackme_gen.py](https://challenge-files.cylabacademy.net/library/5f849d6ff256cc04ade23aa79e9a113659f955147810ef742b7fd39bcf8bb9a3/crackme_gen.py)

Ao abrir o arquivo, foi possível observar a presença de uma variável global chamada `bezos_cc_secret` e de uma função denominada `decode_secret()`, indicando que o código já possuía uma implementação responsável por decodificar o conteúdo armazenado.

[![imagem-2026-11-08-182209122.png](https://i.postimg.cc/SR80rj77/imagem-2026-11-08-182209122.png)](https://postimg.cc/H8pPWYNV)
### Interpretação

Analisando o código, identifiquei que a variável `bezos_cc_secret` armazenava o conteúdo codificado, enquanto a função `decode_secret()` era responsável por realizar sua decodificação.

A partir disso, percebi que não seria necessário desenvolver um algoritmo próprio ou modificar a lógica existente. Bastava chamar a função disponibilizada, passando a variável global como argumento.

### Resolução

Para obter o conteúdo original, bastou adicionar uma chamada à função `decode_secret()`, passando a variável global `bezos_cc_secret` como argumento.

O trecho utilizado foi:

```python
decode_secret(bezos_cc_secret)
```

**Imagem do código após a modificação:**

[![imagem-2026-11-08-182744158.png](https://i.postimg.cc/N0f5zvn9/imagem-2026-11-08-182744158.png)](https://postimg.cc/pm4Wm4RR)


**Resultado obtido:**

Ao executar o arquivo, a própria função realizou a decodificação e imprimiu o resultado diretamente no terminal.
Com o conteúdo decodificado, foi possível identificar a flag solicitada pelo desafio.

> **Flag:** `academy{1m_4_p34nut_a20db6f76f27d8}`

### Conclusão

O desafio **crackme-py** demonstra a importância da análise de código-fonte em atividades de Reverse Engineering.

A resolução consistiu em identificar a variável que armazenava o conteúdo codificado e compreender a função responsável por sua decodificação. Ao perceber que a própria implementação já disponibilizava os recursos necessários, foi possível recuperar a informação com apenas uma chamada de função.

Dessa forma, o desafio reforça que compreender a estrutura e o funcionamento de um programa pode ser suficiente para encontrar soluções simples e eficientes, sem a necessidade de desenvolver código adicional.
