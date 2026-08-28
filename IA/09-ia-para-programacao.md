# 09 — IA para programação

## IA acelera código; você continua responsável

Use IA para reduzir trabalho repetitivo, entender erros e explorar soluções. Não envie código gerado para produção sem revisar, testar e entender o impacto em segurança, desempenho e manutenção.

## Antes de pedir código

Forneça:

- objetivo da funcionalidade;
- linguagem, framework e versões relevantes;
- arquitetura ou estrutura de pastas;
- entradas, saídas e regras de negócio;
- comportamento esperado;
- trecho mínimo reproduzível e mensagem de erro;
- critérios de aceitação;
- testes existentes e limitações.

❌ **Pedido fraco**

> Crie esse sistema.

✅ **Briefing de engenharia**

~~~text
Objetivo: adicionar cadastro de livros.
Stack: Node.js, Express e PostgreSQL.
Estrutura: controller → service → repository.
Regras: ISBN único; título obrigatório; autor deve existir.
Entrega: migration, endpoint POST /livros, validação e testes.
Restrições: não altere endpoints existentes; use parâmetros SQL; não inclua credenciais.
Critérios de aceitação: testes passam, resposta 201 em sucesso e 400/409 nos erros esperados.
Antes de codar, apresente um plano e os arquivos que pretende alterar.
~~~

## Casos de uso

| Tarefa | Prompt inicial útil |
| --- | --- |
| Entender código | “Explique o fluxo desta função, entradas, saídas, efeitos colaterais e riscos” |
| Encontrar bug | “Analise o erro e o trecho mínimo; proponha hipótese, teste e correção” |
| Refatorar | “Preserve a API pública e os testes; reduza duplicação sem mudar comportamento” |
| Testar | “Liste casos normais, limites e falhas; gere testes coerentes com este framework” |
| Documentar | “Documente parâmetros, retorno, erros e exemplo de uso; não invente comportamento” |
| SQL | “Explique o plano lógico desta query e sugira índices somente com justificativa” |
| Git | “Proponha passos Git seguros para esta mudança, incluindo como revisar o diff” |

## Programação por etapas

1. Peça leitura e resumo da arquitetura.
2. Defina a tarefa em critérios de aceitação.
3. Peça plano e lista de arquivos.
4. Implemente uma unidade pequena.
5. Rode testes, linter e build.
6. Revise diff, nomes e casos de erro.
7. Documente a mudança.

## Banco de dados e SQL

Ao usar IA com banco de dados, envie esquema reduzido, relacionamentos e volume aproximado. Peça explicação de impacto antes de comandos destrutivos.

> Revise esta migração PostgreSQL. Verifique compatibilidade, reversão, bloqueios potenciais, integridade referencial e impacto em tabela grande. Não execute nem sugira DROP sem uma alternativa de backup/rollback.

## Segurança de código

- Nunca cole tokens, chaves privadas, senhas ou `.env` completo.
- Revise autenticação, autorização, validação de entrada e consultas parametrizadas.
- Execute dependências e comandos em ambiente controlado.
- Para segurança ofensiva, trabalhe apenas com ambientes autorizados e objetivo defensivo.

## Perguntas de revisão

> Revise este diff como um colega experiente. Separe achados em: bugs, riscos de segurança, desempenho, legibilidade e testes ausentes. Para cada achado, cite o arquivo/trecho e sugira uma correção pequena. Não elogie sem justificar.

Leia [IA em repositórios](./24-ia-em-repositorios.md), [APIs de IA](./23-apis-de-ia.md) e [prompts de programação](./exemplos/prompts-programacao.md).
