# Projeto 6 — Lista de tarefas CLI

> 🟡 **Intermediário**

## Objetivo

Criar CRUD de tarefas em terminal com persistência JSON.

## Funcionalidades

- adicionar tarefa;
- listar pendentes/concluídas;
- concluir e remover por identificador;
- salvar automaticamente;
- carregar sem quebrar se arquivo ainda não existe.

## Arquitetura inicial

\`\`\`text
cli.py → entrada e mensagens
servico.py → regras de tarefas
repositorio.py → leitura/escrita JSON
\`\`\`

## Testes

Teste regras em \`servico.py\` sem usar arquivo. Para persistência, use diretório temporário do pytest. Faça backup/arquivo de teste antes de aprender a escrita.

