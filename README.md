# Node Hcode
NodeJS Hcode - JavaScript runtime built on Chrome's V8 JavaScript engine

## O que é Node
Node não é uma linguagem de programação, é uma plataforma que nos permite executar Javascript no lado do servidor. Para o Javascript funcionar corretamente é necessário um motor de interpretação, esse motor é o V8 do Chrome. O motor V8 é escrito em C++ e é um projeto Open Source, o qual tem a função de fazer a interpretação do Javascript.

## Características do Node
Ryan Dahl, criador do NodeJS estava querendo resolver um problema de assíncronia no Browser e desta necessidade ele observou que o V8 já provia isso, ou seja, uma das principais características do Node que o difere de outras tecnologias (como PHP, Jaba, C#) é a execução das requisições/eventos em single-thread, onde apenas uma Thread (chamada de Event Loop) é responsável por executar o código Javascript. Essa característica leva o nome de I/O não bloqueante, significa que o Javascript executa seus processos de maneira assíncrona.

## Diferenças do Javascript
Uma das diferenças do Javascript é que ele é baseado no contexto, ou seja, se estivermos no lado do client, podemos utilizar recursos de eventos do navegador, como manipular o objeto global window, já isso, não podemos fazer no lado do servidor, porque não temos controle do mouse do usuário, quem tem é o Javascrip no lado do client. Por outro, eu tenho muitos recursos no lado do servidor que não podemos utilizar no lado do client, como por exemplo a manipulação de diretórios e arquivos do Sistema Operacional.

## Como o Node é estruturado? 
- Core Concepts - São conceitos fundamentais, como: I/O não bloqueante, Eventos, Event Loop, Times
- API's Nativas - São as API'S que já vem com o node como: Criptografia, gerenciamento de arquivos, conexões do DP e do Path.
- API's de Terceiros - São recursos que a comunidade cria para facilitar uma demanda do node, como: Express, Body Parser, estes módulos externos são gerenciados pelo NPM (Node Package Maneger).

## Primeiro Exemplo com Node
Criando um servidor node

```

const http = require('http')
const host = '127.0.0.1'
const port = '3000'

const server = createServer((req, res) => {
    res.statusCode = 200
    res.setHeader('Content-Type', 'text/plain')
    res.end('Olá Mundo \n Meu Primeiro Script')
})

server.listen(host, port, () => {
    console.log(`Server running at http://${host}:
    ${port}`)
})

```