# Desafio — sistema de biblioteca CLI

## Problema

Uma pequena biblioteca quer controlar livros e empréstimos em terminal.

## Requisitos base

- cadastrar livro com título, autor e identificador;
- listar livros disponíveis;
- emprestar apenas livro disponível;
- devolver livro emprestado;
- salvar e carregar dados em JSON.

## Nível 2

- buscar por título/autor;
- impedir IDs duplicados;
- registrar data de empréstimo;
- permitir vários usuários fictícios.

## Nível 3

- separar interface, serviço e persistência;
- usar testes com diretório temporário;
- validar JSON malformado;
- registrar operações em logging sem dados sensíveis;
- criar README e instruções de execução.

## Perguntas de projeto

- O que identifica um livro de forma única?
- Que operações devem ser atômicas?
- Como seu programa reage a arquivo inexistente?
- Que função deve ser pura e fácil de testar?

Não abra uma solução antes de projetar seus próprios modelos e testes.

