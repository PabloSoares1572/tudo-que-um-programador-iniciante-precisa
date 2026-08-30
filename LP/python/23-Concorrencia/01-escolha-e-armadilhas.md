# Escolha e armadilhas de concorrência

## Comece sequencial

Antes de introduzir concorrência, meça e escreva a versão sequencial correta. Concorrência aumenta dificuldade de teste, logs, tratamento de falha e encerramento.

## Armadilhas

- **race condition:** resultado depende da ordem imprevisível de acesso;
- **deadlock:** tarefas ficam esperando recursos umas das outras;
- **bloqueio:** chamada síncrona longa trava loop async;
- **cancelamento incompleto:** tarefa continua depois que a aplicação deveria parar;
- **exceção perdida:** falha em tarefa de fundo não é observada.

## Regras úteis

1. Limite a concorrência; não dispare milhares de requisições de uma vez.
2. Defina timeout, cancelamento e retry com backoff quando fizer sentido.
3. Mantenha I/O separado de regra de negócio para testar.
4. Use filas/estruturas seguras quando houver estado compartilhado.
5. Registre contexto sem registrar dados sensíveis.

← [Concorrência](./README.md) | [Performance →](../24-Performance/README.md)

