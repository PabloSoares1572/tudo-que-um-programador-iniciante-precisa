# Desafio — refatorar sem quebrar

## Cenário

Você recebeu um arquivo com uma função de 150 linhas que lê entrada, calcula total, grava arquivo e imprime mensagens. A função funciona em casos simples, mas ninguém consegue alterar com confiança.

## Tarefa

1. Escreva testes de caracterização do comportamento atual.
2. Identifique responsabilidades distintas.
3. Extraia funções pequenas sem mudar resultados.
4. Troque valores mágicos por nomes/configuração.
5. Adicione validação e mensagens de erro específicas.
6. Documente decisões e o que ficou fora do escopo.

## Nível profissional

- use type hints úteis;
- preserve compatibilidade pública ou crie plano de migração;
- faça commits pequenos;
- compare cobertura antes/depois;
- não “refatore” junto com mudança grande de regra de negócio.

O objetivo é aprender que qualidade não é reescrever tudo: é reduzir risco em passos verificáveis.

