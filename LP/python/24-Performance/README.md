# 24 — Performance, complexidade e profiling

> 🔴 **Avançado**

A regra é: **meça antes de otimizar**. Um programa lento pode estar esperando rede, lendo disco, usando estrutura inadequada ou repetindo uma consulta; trocar uma linha por uma versão “esperta” sem dados geralmente piora legibilidade.

## Complexidade (Big O)

| Complexidade | Exemplo |
| --- | --- |
| O(1) | acessar chave de dicionário em caso típico |
| O(n) | percorrer todos os itens |
| O(log n) | busca binária em dados ordenados |
| O(n²) | comparar cada item com cada outro item |

Big O descreve crescimento, não tempo exato. Dados pequenos, I/O e implementação também importam.

## Técnicas úteis

- escolha estrutura adequada: set/dict para busca frequente, quando aplicável;
- use generators para fluxo grande que não precisa estar todo em memória;
- evite N+1 em banco de dados;
- faça cache apenas com política de invalidação;
- use profiling para localizar gargalo real.

## Índice

- [Profiling e otimização responsável](./01-profiling-e-otimizacao.md)
- [Algoritmos e estruturas de dados](./02-algoritmos-e-estruturas.md)

← [Concorrência](../23-Concorrencia/README.md) | [Segurança →](../25-Seguranca/README.md)

