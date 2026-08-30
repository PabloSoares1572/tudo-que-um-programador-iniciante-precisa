# PostgreSQL, ORM e segurança de queries

## Quando avançar para PostgreSQL

PostgreSQL é um banco relacional completo, comum em aplicações web e produção. Avance depois de compreender tabelas, índices, joins, transações e consultas SQL básicas. Use documentação oficial e uma configuração local/contêiner de desenvolvimento; nunca aponte exercícios a banco de produção.

## Transações

Uma transação evita que operações relacionadas fiquem pela metade. Por exemplo, criar pedido e reduzir estoque devem ter política consistente para falhas e concorrência. Não espalhe commits aleatórios em cada linha; defina a fronteira da operação.

## ORM

ORM mapeia objetos para tabelas e pode acelerar desenvolvimento, mas não elimina SQL, índices, transações ou problemas de desempenho. Estude primeiro a consulta que o ORM produz e faça migrações versionadas.

## SQL Injection

Inseguro:

\`\`\`python
# NÃO FAÇA: entrada pode alterar a consulta
consulta = "SELECT * FROM usuarios WHERE nome = '" + nome + "'"
\`\`\`

Seguro: use parâmetros da biblioteca/driver, exatamente como no exemplo SQLite do módulo anterior. Validação de entrada e permissões mínimas do usuário do banco complementam parametrização.

← [Banco de dados](./README.md) | [APIs →](../20-APIs/README.md)

