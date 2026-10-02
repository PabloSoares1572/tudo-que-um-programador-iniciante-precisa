# Estratégia de testes para um projeto

1. Escreva funções com entradas e saídas claras.
2. Teste primeiro regras de negócio puras, sem arquivo, rede ou banco.
3. Acrescente testes de integração onde a fronteira importa.
4. Faça testes fim a fim apenas para fluxos críticos.
5. Reproduza cada bug corrigido em um teste.

## Evite

- testes que dependem de ordem ou dados externos reais;
- chamar serviços pagos/produção no teste;
- dormir com `time.sleep` para esperar comportamento assíncrono;
- testar detalhes privados que impedem refatoração.

Use dados descartáveis, banco de teste e variáveis de ambiente separadas. A documentação do projeto deve explicar como executar os testes localmente e em CI.

← [Fixtures e mocks](./01-fixtures-mocks-e-cobertura.md) | [Debugging →](../17-Debugging/README.md)
