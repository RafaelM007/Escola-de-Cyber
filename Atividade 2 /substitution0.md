# substitution0

> Autor: **Rafael Moreira Xavier**
>
> Categoria: Criptografia

### Introdução

O desafio **substitution0**, disponibilizado pelo CYLAB, consiste em decifrar uma mensagem que foi criptografada utilizando uma cifra de substituição.

O objetivo é identificar a chave utilizada na criptografia e aplicá-la para recuperar o texto original e encontrar a flag.

### Análise Inicial

O enunciado do desafio é:

> Chegou uma mensagem, mas parece estar toda embaralhada. Felizmente parece que sim tenha a chave no início. Você consegue decifrar essa cifra de substituição?

O arquivo disponibilizado contém uma mensagem aparentemente sem sentido, acompanhada de uma sequência de caracteres no início:

[message.txt](https://challenge-files.cylabacademy.net/library/ba4dc472a6e0784e2ec4ad7184bdbe107b432edfc1464d836433b8eb16279406/message.txt)

Ao analisar o conteúdo, percebi que a primeira linha apresentava uma sequência de 26 letras:

```text
KCXZUNDAOYVRHWLGFSIMQPTEBJ
```

Como o alfabeto possui 26 letras, suspeitei que essa sequência representasse a chave de substituição utilizada para criptografar a mensagem.

### Interpretação

Uma cifra de substituição consiste em substituir cada letra do alfabeto por outra, seguindo um mapeamento definido por uma chave.

Nesse caso, a sequência encontrada no início do arquivo apresentava exatamente 26 caracteres, correspondentes às letras do alfabeto.

Isso indicou que a sequência poderia ser utilizada como chave para realizar a substituição inversa e recuperar o texto original.

Para facilitar o processo, optei por utilizar o **CyberChef**, que disponibiliza operações de manipulação e decodificação de textos.

### Resolução

Primeiramente, copiei o conteúdo da mensagem e o inseri no CyberChef.

Como o texto apresentava letras maiúsculas e minúsculas, utilizei a operação **To Lower case** para padronizar todos os caracteres em letras minúsculas.

Em seguida, utilizei a operação **Substitute**, responsável por realizar a substituição de caracteres, configurando o mapeamento com base na sequência de 26 letras identificada no início do arquivo.
Após configurar a substituição, executei a operação e obtive a mensagem em texto legível.

[![imagem-2026-11-08-201745997.png](https://i.postimg.cc/9XNB2CHQ/imagem-2026-11-08-201745997.png)](https://postimg.cc/RqKtQr0k)

Ao final da mensagem, encontrei a flag solicitada pelo desafio:

> **Flag:** `academy{5ub5717u710n_3v0lu710n_1ddf0d6c}`

### Conclusão

O desafio **substituição0** demonstra a aplicação de cifras de substituição e a importância de identificar padrões presentes em mensagens criptografadas.

A principal pista foi a sequência de 26 letras encontrada no início do arquivo, que indicava a existência de uma chave de substituição alfabética.

Utilizando o CyberChef, foi possível padronizar o texto e aplicar a substituição inversa para recuperar a mensagem original e encontrar a flag.

Dessa forma, o desafio reforça a importância de observar possíveis chaves fornecidas no próprio arquivo e compreender como funcionam os mecanismos básicos de substituição de caracteres.
