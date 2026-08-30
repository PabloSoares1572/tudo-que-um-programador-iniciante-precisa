# Profiling e otimização responsável

## Processo

\`\`\`text
Definir métrica → reproduzir cenário → medir → localizar gargalo
→ aplicar mudança pequena → medir novamente → manter ou reverter
\`\`\`

Métricas podem ser tempo, memória, número de queries, latência p95 ou custo. Escolha uma que represente o problema do usuário.

## Ferramentas

- \`timeit\`: comparar pequenos trechos com cuidado;
- \`cProfile\`: identificar onde o programa passa tempo;
- ferramentas do banco: consultas e índices;
- métricas/logs: observar em produção sem expor dados.

## Não faça

- otimização “porque parece mais rápida”;
- micro-otimização antes de resolver algoritmo ruim;
- cache infinito sem expiração e limite;
- desativar validação/testes para ganhar números artificiais.

## Exemplo de escolha

Para verificar muitos IDs únicos, criar um \`set\` pode tornar buscas repetidas mais adequadas do que procurar em lista a cada vez. Mas se a coleção tem três itens e a operação é rara, a clareza pode valer mais que a microdiferença.

← [Performance](./README.md) | [Algoritmos →](./02-algoritmos-e-estruturas.md)

