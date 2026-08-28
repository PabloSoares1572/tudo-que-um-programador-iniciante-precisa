# 24 — IA trabalhando em repositórios

## Uma boa tarefa começa antes do código

Quando uma IA ou agente tem acesso a um repositório, o maior risco é modificar algo sem entender dependências, padrões ou testes. Dê instruções de exploração e critérios de aceitação antes de pedir implementação.

## Protocolo de trabalho

~~~text
Antes de modificar qualquer arquivo:

1. Analise a estrutura do projeto.
2. Identifique tecnologias, scripts e convenções.
3. Leia README, documentação e arquivos relevantes.
4. Localize testes e regras de qualidade.
5. Resuma o entendimento e proponha um plano.
6. Liste arquivos que serão criados ou alterados.
7. Só então implemente em uma branch apropriada.
8. Execute testes, linter, build ou validações disponíveis.
9. Corrija problemas encontrados.
10. Entregue resumo, diff, riscos e passos de validação.

Nunca acesse segredos, altere infraestrutura, apague arquivos ou faça deploy fora do escopo sem confirmação explícita.
~~~

## Especificação de tarefa

| Campo | Exemplo |
| --- | --- |
| Objetivo | “Adicionar filtro por categoria na lista de produtos” |
| Escopo | “Somente frontend e endpoint já existente” |
| Stack | “React, TypeScript, API REST” |
| Regras | “Filtro combina com busca por nome” |
| Fora de escopo | “Não alterar schema de banco” |
| Critérios | “Testes passam; estado vazio possui mensagem” |
| Validação | “npm test e npm run build” |

## Prompt completo

~~~text
Objetivo: [mudança].
Antes de editar, leia a estrutura e os arquivos relacionados; explique o fluxo atual.
Respeite padrões existentes de nomes, estilo e arquitetura.
Crie um plano curto com arquivos afetados e riscos.
Implemente apenas o escopo descrito.
Adicione/ajuste testes quando houver padrão no projeto.
Execute as validações disponíveis e informe o resultado real.
No final, entregue: resumo, arquivos modificados, como testar e pendências.
Não faça commits, merges, deploys, mudanças de dependência ou alterações fora do escopo sem confirmação.
~~~

## Revisão do diff

Peça uma leitura independente:

> Revise este diff. Procure regressões, tratamento de erro ausente, riscos de segurança, quebra de compatibilidade, testes ausentes e documentação desatualizada. Classifique achados por severidade e não invente problemas sem apontar o trecho.

## Permissões e segurança

Uma IA com acesso a repositório pode ver conteúdo privado. Limite escopo e prefira permissões de leitura durante análise. Não exponha arquivos de ambiente, chaves ou configurações sensíveis. Use branch e revisão para tornar a mudança rastreável.

Veja também [Agentes](./20-agentes-de-ia.md) e [IA para programação](./09-ia-para-programacao.md).
