# Guia de Referência Rápida — JavaScript

Este arquivo reúne todos os comandos, funções, palavras-chave e conceitos mencionados em nossas conversas sobre **JavaScript**.  
Eles estão organizados em categorias para facilitar sua consulta. Sempre que surgirem novos termos, a tabela será atualizada!

---

## Índice de Categorias

- [Declaração de Variáveis](#declaração-de-variáveis)
- [Funções](#funções)
- [Objetos Globais do Navegador (BOM/DOM)](#objetos-globais-do-navegador-bomdom)
- [Manipulação de String/Array](#manipulação-de-stringarray)
- [Template String / Interpolação](#template-string--interpolação)
  - [Caracteres Especiais em Interpolação](#caracteres-especiais-em-interpolação)
  - [Conjuntos de Interpolação](#conjuntos-de-interpolação)
- [Cookies](#cookies)
- [Estruturas de Controle](#estruturas-de-controle)
- [Datas e Horas](#datas-e-horas)

---

## 📦 Declaração de Variáveis

| Palavra/Comando     | Origem do Nome         | O que faz / Para que serve?                                                                                   |
|---------------------|-----------------------|---------------------------------------------------------------------------------------------------------------|
| `let`               | "let it be" (deixe ser)| Declara uma variável que pode ter seu valor alterado depois da declaração.                                    |
| `const`             | "constant" (constante)| Declara uma variável constante, que NÃO pode ser reatribuída.                                                 |

---

## 🛠️ Funções

| Palavra/Comando          | Origem do Nome                                | O que faz / Para que serve?                                                                     |
|--------------------------|-----------------------------------------------|-------------------------------------------------------------------------------------------------|
| `function`               | Do inglês "função"                            | Declara uma função, bloco de código reutilizável.                                               |
| `setInterval()`          | "set"=definir, "interval"=intervalo           | Executa uma função repetidas vezes em um intervalo de tempo.                                    |
| `setTimeout()`           | "set"=definir, "timeout"=tempo limite         | Executa uma função uma única vez após X milissegundos.                                          |
| `push()`                 | "push"=empurrar                               | Adiciona um elemento ao final de um array.                                                      |
| `split()`                | "split"=dividir                               | Divide uma string em partes, baseado em um separador.                                           |
| `substring()`            | "sub"=sub, "string"=cadeia de caracteres      | Retorna parte de uma string entre dois índices.                                                 |
| `indexOf()`              | "index"=índice, "of"=de                       | Retorna o índice da primeira ocorrência de um valor em uma string/array.                        |

---

## 🌐 Objetos Globais do Navegador (BOM/DOM)

| Palavra/Comando     | Origem do Nome           | O que faz / Para que serve?                                                                             |
|---------------------|-------------------------|---------------------------------------------------------------------------------------------------------|
| `window`            | Janela do navegador     | Objeto global que representa a janela do navegador.                                                     |
| `document`          | Documento HTML          | Objeto que representa a página HTML carregada no navegador.                                             |
| `location`          | Localização             | Objeto que representa/permite manipular a URL da página.                                                |
| `location.reload()` | "reload"=recarregar     | Recarrega a página atual.                                                                               |
| `console.log()`     | "console"=console, "log"=registrar | Exibe mensagens no console do navegador (usado para depuração).                            |

---

## 🔡 Manipulação de String/Array

| Palavra/Comando     | Origem do Nome           | O que faz / Para que serve?                                                                             |
|---------------------|-------------------------|---------------------------------------------------------------------------------------------------------|
| `split()`           | "split"=dividir         | Divide uma string em partes, baseado em um separador.                                                   |
| `push()`            | "push"=empurrar         | Adiciona um elemento ao final de um array.                                                              |
| `substring()`       | "sub"=sub, "string"=cadeia | Retorna parte de uma string entre dois índices.                                                     |
| `indexOf()`         | "index"=índice, "of"=de | Retorna o índice da primeira ocorrência de um valor em uma string/array.                                |

---

## 📝 Template String / Interpolação

| Palavra/Comando   | Origem do Nome                 | O que faz / Para que serve?                                                                              |
|-------------------|-------------------------------|----------------------------------------------------------------------------------------------------------|
| `` `${}` ``         | Interpolação de variável      | Permite inserir valores de variáveis/expressões dentro de strings usando crases (``).                   |

### Caracteres Especiais em Interpolação

| Caractere/Símbolo | Nome/Significado no contexto | O que faz na interpolação/JS?                                                                                                       |
|-------------------|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `` ` ``           | Crase (backtick)             | Delimita o início e o fim de uma template string, permitindo interpolação de variáveis.                                             |
| `${}`             | Placeholder de variável       | Onde você coloca uma variável ou expressão JS para ser avaliada e inserida na string.                                               |
| `$`               | Sinal de dólar                | Parte obrigatória na sintaxe da interpolação, indica o início do placeholder.                                                       |
| `{}`              | Chaves                        | Delimitam a expressão ou variável a ser avaliada/interpolada na string.                                                            |
| `#`               | Hash (jogo da velha)          | Em URLs, indica o início do fragmento (ex: `/pagina#/test`). Em strings JS, é apenas um símbolo, mas pode ser interpolado normalmente.|
| `?`               | Interrogação                  | Em URLs, indica o início da query string (ex: `/pagina?/search`). Em JS, é só um caractere comum, aparece em buscas e parâmetros.    |
| `/`               | Barra                         | Símbolo de separação de diretórios em caminhos e URLs.                                                                              |

#### Exemplos:

```js
const rota = "test";
const url1 = `#/test`;
const busca = "search";
const url2 = `?/search`;
const custom = `${rota}-${busca}`; // "test-search"
const url3 = `#/test?busca=${busca}`; // "#/test?busca=search"
```

- Qualquer caractere pode ser interpolado, desde que esteja dentro das crases e, para variáveis, dentro de `${}`.
- Diferentes caracteres (`#`, `?`, `/`) possuem significado especial em URLs, mas na interpolação JS são tratados como texto.

### Conjuntos de Interpolação

Você pode juntar vários caracteres e variáveis na mesma template string:

```js
const rota = "test";
const busca = "search";
const url = `#/test?busca=${busca}`; // "#/test?busca=search"
const urlDinamica = `#/${rota}?/search`;
```

---

## 🍪 Cookies

| Palavra/Comando              | Origem do Nome                                   | O que faz / Para que serve?                                                                                      |
|------------------------------|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| `document.cookie`            | "document"=documento, "cookie"=bolacha           | Permite ler, criar, modificar e apagar cookies do navegador.                                                     |
| `encodeURI()`                | "encode"=codificar, "URI"=identificador de recurso| Codifica caracteres especiais de uma URI (endereços).                                                            |
| `encodeURIComponent()`       | "encode"=codificar, "URIComponent"=componente da URI | Codifica partes da URI, ideal para valores de parâmetros/cookies.                                            |
| `decodeURIComponent()`       | "decode"=decodificar, "URIComponent"=componente da URI | Decodifica o valor que foi codificado por encodeURIComponent().                                             |
| `path=/` (no cookie)         | "path"=caminho, "/"=raiz                         | Define o caminho (endereço) em que o cookie está disponível.                                                     |
| `expires=` (no cookie)       | "expires"=expira                                 | Define a data de expiração do cookie.                                                                            |
| `;` (ponto e vírgula nos cookies) | Separador                                   | Separa atributos diferentes dentro de um cookie (nome, valor, expiração, caminho, etc).                          |

---

## 🔄 Estruturas de Controle

| Palavra/Comando   | Origem do Nome           | O que faz / Para que serve?                                                                  |
|-------------------|-------------------------|----------------------------------------------------------------------------------------------|
| `if/else`         | "if"=se, "else"=senão   | Estrutura para decisões/condições no código.                                                 |
| `for`             | "for"=para              | Estrutura de repetição (loop), para executar código várias vezes.                            |
| `while`           | "while"=enquanto        | Estrutura de repetição que executa enquanto a condição for verdadeira.                       |

---

## 📅 Datas e Horas

| Palavra/Comando     | Origem do Nome                | O que faz / Para que serve?                                                                           |
|---------------------|------------------------------|-------------------------------------------------------------------------------------------------------|
| `Date()`            | "Date"=data                  | Cria um objeto para manipular datas e horários.                                                       |
| `setFullYear()`     | "set"=definir, "FullYear"=ano completo | Define o ano de um objeto Date.                                                               |
| `toUTCString()`     | "to"=para, "UTCString"=string UTC | Converte a data para uma string no formato UTC (usada para expiração de cookies).                |

---
