# Node Hcode
NodeJS Hcode - JavaScript runtime built on Chrome's V8 JavaScript engine

## O que é Nodejs
Node não é uma linguagem de programação, é uma plataforma que nos permite executar Javascript no lado do servidor. Para o Javascript funcionar corretamente é necessário um motor de interpretação, esse motor é o V8 do Chrome. O motor V8 é escrito em C++ e é um projeto Open Source, o qual tem a função de fazer a interpretação do Javascript.

## Características do Node
Ryan Dahl, criador do NodeJS estava querendo resolver um problema de assíncronia no Browser e desta necessidade ele observou que o V8 já provia isso, ou seja, uma das principais características do Node que o difere de outras tecnologias (como PHP, Jaba, C#) é a execução das requisições/eventos em single-thread, onde apenas uma Thread (chamada de Event Loop) é responsável por executar o código Javascript. Essa característica leva o nome de I/O não bloqueante, significa que o Javascript executa seus processos de maneira assíncrona. 