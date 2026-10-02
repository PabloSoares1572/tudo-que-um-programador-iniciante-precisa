# Computador, programa e algoritmo

## Explicação simples

Um computador é uma máquina que executa instruções. Ele não “entende intenção”: precisa que os passos estejam claros e na ordem correta. Um **programa** é um conjunto dessas instruções; um **algoritmo** é o plano de passos para resolver um problema, mesmo antes de escrever código.

## Explicação técnica

- **Hardware:** parte física, como CPU, memória RAM, SSD, teclado e placa de vídeo.
- **Software:** programas e dados executados pelo hardware.
- **Sistema operacional:** software que administra hardware e permite que outros programas rodem.
- **Código-fonte:** texto escrito por uma pessoa em uma linguagem de programação.
- **Interpretador:** programa que lê/executa código Python. A implementação mais comum é o **CPython**.

## Algoritmo antes do código

Problema: calcular a média de duas notas.

```text
1. Receber nota 1
2. Receber nota 2
3. Somar as notas
4. Dividir por 2
5. Mostrar a média
```

O código Python será uma tradução precisa desse raciocínio. Se o algoritmo estiver errado, escrever em uma linguagem diferente não o conserta.

## Entrada, processamento e saída

| Parte | Exemplo da média |
| --- | --- |
| Entrada | `7.5` e `9.0` |
| Processamento | soma e divisão |
| Saída | `8.25` |

## Compilada ou interpretada?

Essa é uma simplificação útil: linguagens compiladas normalmente transformam código para outra forma antes de executar; linguagens interpretadas são executadas por um interpretador. Python costuma ser chamado de interpretado, mas o CPython também gera bytecode internamente. Para começar, guarde o essencial: você executará o arquivo usando o interpretador Python.

## Bug e debugging

Um **bug** é um defeito no programa. Pode ser erro de sintaxe, regra de negócio errada ou comportamento inesperado. **Debugging** é investigar, reproduzir, isolar e corrigir a causa — não é adivinhar e trocar linhas aleatoriamente.

## Atividade

Escreva, em português, um algoritmo para calcular o valor final de uma compra com desconto. Identifique entrada, processamento e saída antes de tocar em Python.

← [Introdução](./README.md) | [Python e versões →](./02-python-origem-e-versoes.md)
