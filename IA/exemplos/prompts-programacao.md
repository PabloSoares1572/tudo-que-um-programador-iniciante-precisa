# Prompts para programação

## 1. Entender repositório

~~~text
Analise a estrutura deste projeto antes de sugerir mudanças.
Identifique stack, pontos de entrada, scripts, testes e convenções.
Depois explique o fluxo relacionado a [funcionalidade] e liste os arquivos que preciso ler.
Não altere arquivos nem presuma dependências não encontradas.
~~~

## 2. Investigar bug

~~~text
Stack: [linguagem/framework/versão].
Comportamento esperado: [esperado].
Comportamento atual: [atual].
Erro: [mensagem].
Trecho mínimo: [código].
Primeiro proponha até 3 hipóteses, com teste para confirmar cada uma.
Só depois sugira uma correção pequena e testes de regressão.
~~~

## 3. Criar funcionalidade

~~~text
Objetivo: [funcionalidade].
Stack: [stack]. Arquitetura: [padrão].
Entradas, saídas e regras: [detalhes].
Critérios de aceitação: [lista].
Antes de codar, apresente plano e arquivos afetados.
Preserve APIs existentes, não exponha segredos e inclua testes coerentes com o projeto.
~~~

## 4. Revisar código

~~~text
Revise este diff como revisor técnico.
Procure bugs, riscos de segurança, tratamento de erro, desempenho, legibilidade e testes ausentes.
Para cada achado: severidade, arquivo/trecho, motivo e correção sugerida.
Não invente problemas; marque elogios somente quando houver evidência.

[diff]
~~~

## 5. Refatorar

~~~text
Refatore este código para reduzir duplicação e melhorar legibilidade.
Preserve comportamento público e compatibilidade.
Antes, explique os problemas atuais. Depois, mostre patch, justificativa e testes necessários.
Não faça otimizações prematuras nem mude dependências sem motivo.

[código]
~~~

## 6. Criar testes

~~~text
Com base nesta função e nos requisitos, crie testes em [framework].
Cubra caso normal, limites, entrada inválida, erro externo e regressão conhecida.
Explique o objetivo de cada caso. Não teste detalhes internos que possam mudar sem afetar comportamento.

[código/requisitos]
~~~

## 7. SQL e banco de dados

~~~text
Banco: [PostgreSQL/MySQL/etc.].
Esquema relevante: [tabelas/colunas/chaves].
Objetivo: [consulta ou migração].
Gere SQL parametrizável e explique impacto em índices, integridade e reversão.
Não use DROP/DELETE amplo sem avisar riscos e propor uma forma segura de validar.
~~~

## 8. Documentar API

~~~text
Documente este endpoint para quem vai integrá-lo.
Inclua método, rota, autenticação, parâmetros, corpo, respostas de sucesso/erro, exemplos e limites conhecidos.
Não invente campos. Marque dúvidas que dependem da equipe responsável.

[código/contrato]
~~~

## 9. Git e GitHub

~~~text
Preciso realizar esta mudança no Git: [situação].
Explique os passos seguros, o que cada comando faz, como revisar o diff e como desfazer apenas se necessário.
Não sugira comandos destrutivos sem explicar o impacto e uma alternativa recuperável.
~~~

## 10. Plano de deploy

~~~text
Crie um plano de deploy para [mudança] em [ambiente].
Inclua pré-requisitos, backup/rollback, testes pós-deploy, observabilidade e responsável pela aprovação.
Não execute comandos nem presuma acesso à produção.
~~~

Leia [IA para programação](../09-ia-para-programacao.md) e [IA em repositórios](../24-ia-em-repositorios.md).
