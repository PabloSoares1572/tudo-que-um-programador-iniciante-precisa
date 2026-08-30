# Projeto final — Plataforma de gestão de tarefas

> ⚫ **Profissional/Especialista**

## Especificação

Crie uma plataforma de tarefas para equipes fictícias. Ela deve permitir cadastrar projeto, tarefas, prioridades, responsáveis e status. O sistema pode começar como API e ganhar interface web depois.

## Requisitos funcionais

- CRUD de projetos e tarefas;
- filtros por status/prioridade/responsável;
- histórico de mudanças;
- paginação;
- autenticação/autorização adequada ao cenário;
- API documentada;
- persistência relacional.

## Requisitos não funcionais

- ambiente virtual e dependências reproduzíveis;
- configuração por ambiente;
- segredos fora do Git;
- logs sem dados sensíveis;
- testes unitários e de integração;
- tratamento de erros;
- README, diagrama simples e changelog;
- CI básica, se possível.

## Milestones

1. requisitos e modelo de dados;
2. regras puras + testes;
3. persistência e migrações;
4. API/rotas;
5. autenticação/autorização;
6. observabilidade e segurança;
7. documentação e deploy de demonstração.

## Dicas

Comece com uma única entidade e um endpoint. Faça cada milestone passar testes antes do próximo. Não tente implementar autenticação, frontend, filas e cache no primeiro dia.

## Solução de referência (arquitetura, não código pronto)

\`\`\`text
app/
  api/          → rotas e schemas
  services/     → regras de negócio
  repositories/ → persistência
  domain/       → entidades/contratos
  config/       → leitura de ambiente
tests/
\`\`\`

Essa é apenas uma possibilidade. Justifique qualquer estrutura com base no tamanho e nas responsabilidades reais do seu projeto.

