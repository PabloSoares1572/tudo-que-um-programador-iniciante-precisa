# Algoritmos e estruturas de dados

Esta é uma trilha de compreensão, não uma competição de decorar entrevistas.

## Fundamentos

- **stack/pilha:** último a entrar, primeiro a sair; use lista com \`append\`/\`pop\` no fim.
- **queue/fila:** primeiro a entrar, primeiro a sair; \`collections.deque\` é apropriado.
- **hash map:** dicionário; busca por chave em caso típico é eficiente.
- **set:** unicidade e operações de conjunto.
- **linked list:** importante conceitualmente; listas Python não são linked lists.
- **tree/árvore:** hierarquia, como diretórios.
- **graph/grafo:** nós e relações, como rotas/rede.

## Busca e ordenação

Use \`sorted\` e \`.sort()\` antes de implementar ordenação manual. Entenda busca linear e binária, mas não reescreva algoritmo de biblioteca para uso comum. Para graphs, aprenda BFS/DFS com exemplos pequenos e teste ciclos/dados desconectados.

## Recursão

Uma função recursiva chama a si mesma e precisa de caso base. Em Python, profundidade de recursão é limitada; uma solução iterativa é muitas vezes mais segura para entradas grandes.

## Prática

Implemente fila com \`deque\`, um contador de palavras com \`Counter\` e uma busca em árvore de diretórios fictícia. Meça e explique a escolha de cada estrutura.

← [Profiling](./01-profiling-e-otimizacao.md) | [Segurança →](../25-Seguranca/README.md)

