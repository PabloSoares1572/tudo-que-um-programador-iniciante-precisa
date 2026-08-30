# 19 — Banco de dados com Python

> 🟡 **Intermediário → ⚫ Profissional**

Banco de dados guarda informação estruturada e permite consultá-la. Antes de usar ORM, entenda SQL e modelagem básica.

## Conceitos

| Termo | Ideia |
| --- | --- |
| tabela | conjunto de registros do mesmo tipo |
| linha | um registro |
| coluna | atributo do registro |
| chave primária | identifica uma linha de forma única |
| chave estrangeira | relaciona tabelas |
| CRUD | criar, ler, atualizar e apagar |
| transação | conjunto de operações que deve ser consistente |

## SQLite para aprender

SQLite vem na biblioteca padrão e armazena o banco em arquivo. É ótimo para estudo, protótipos e cenários compatíveis, mas não é automaticamente a melhor escolha para todo sistema multiusuário.

\`\`\`python
import sqlite3

with sqlite3.connect("tarefas.db") as conexao:
    conexao.execute(
        "CREATE TABLE IF NOT EXISTS tarefas (id INTEGER PRIMARY KEY, titulo TEXT NOT NULL)"
    )
    conexao.execute("INSERT INTO tarefas (titulo) VALUES (?)", ("Estudar Python",))
\`\`\`

O \`?\` é parâmetro de query. Nunca monte SQL com f-string ou concatenação usando entrada do usuário.

## Índice

- [PostgreSQL, transações e ORM](./01-postgresql-orm-e-seguranca.md)
- [Projeto CRUD](../Projetos/08-crud-sqlite.md)

← [Ambientes](../18-Ambientes-e-Dependencias/README.md) | [APIs →](../20-APIs/README.md)

