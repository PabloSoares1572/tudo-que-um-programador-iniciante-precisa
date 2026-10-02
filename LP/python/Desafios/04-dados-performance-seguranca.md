# Desafio — dados, performance e segurança

## Cenário

Um programa importa CSV grande de pedidos, valida campos, grava no banco e gera relatório. Ele está lento, falha em entradas ruins e registra dados sensíveis em log.

## Tarefa

- defina métrica de desempenho antes de mudar o código;
- processe dados em lotes/fluxo quando necessário;
- valide schema e limite tamanho/linhas;
- use transações e queries parametrizadas;
- crie logs úteis sem CPF, e-mail, token ou cartão;
- faça testes com CSV válido, vazio, malformado e grande;
- documente como executar em ambiente de teste.

## Discussão

Explique se generator, cache, índice de banco, fila ou concorrência ajuda — e prove com medição. A melhor solução pode ser mais simples que o recurso avançado.

