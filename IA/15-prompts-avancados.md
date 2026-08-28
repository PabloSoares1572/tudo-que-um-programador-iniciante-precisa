# 15 — Prompts avançados e saídas estruturadas

## Quando um prompt precisa virar especificação

Tarefas com regras, várias etapas ou integração com sistemas ganham qualidade quando você escreve uma especificação. O objetivo é reduzir ambiguidades e tornar a resposta testável.

## Especificação curta e forte

~~~text
Tarefa: [verbo + entrega].
Público/consumidor: [quem usará].
Entradas disponíveis: [dados/documentos].
Regras de negócio: [lista].
Fora de escopo: [o que não fazer].
Critérios de aceitação: [como validar].
Formato: [estrutura exata].
Plano: apresente antes de executar se a tarefa alterar arquivos, dados ou recursos externos.
~~~

## Markdown, tabela e JSON

Escolha o formato pelo destino:

| Destino | Formato melhor | Validação |
| --- | --- | --- |
| Leitura humana | Markdown com títulos e listas | Revisão visual |
| Comparação | Tabela | Campos completos e coerentes |
| Sistema | JSON com esquema | Parser/validador |
| Planilha | CSV ou tabela | Importação e tipos |
| Código | Arquivos com nomes e testes | Build, linter e testes |

### Exemplo de JSON

~~~text
Classifique cada item abaixo.
Retorne somente JSON válido conforme o esquema:
{
  "itens": [
    {"id": "string", "categoria": "alta|media|baixa", "motivo": "string"}
  ]
}
Regras: não crie IDs; use categoria "baixa" quando não houver evidência suficiente.
~~~

O modelo pode errar aspas, campos ou JSON. Sempre valide em código antes de usar a saída automaticamente.

## Templates reutilizáveis

Crie prompts com variáveis explícitas:

~~~text
Você é [papel útil].
Objetivo: [objetivo].
Contexto: [contexto relevante].
Entrada: <entrada>[conteúdo]</entrada>
Entregue: [formato].
Critérios: [itens verificáveis].
Quando faltar dado, [pergunte / use null / registre a lacuna].
~~~

Salve uma versão com exemplo de entrada e saída esperada. Isso facilita ajustar o template sem perder consistência.

## Prompt para revisão por rubrica

> Avalie a entrega usando os critérios abaixo: corretude, completude, clareza e aderência ao escopo. Dê evidência textual para cada nota. Em seguida, proponha uma revisão mínima. Não trate a própria avaliação como confirmação de verdade: sinalize itens que exigem teste ou fonte externa.

## O que não fazer

- Pedir “faça tudo perfeitamente” sem critérios.
- Misturar instruções contraditórias.
- Exigir uma ferramenta que a plataforma não possui.
- Colocar dados secretos em template compartilhável.
- Automatizar ações irreversíveis sem etapa de aprovação.

Complementos: [Técnicas avançadas](./26-tecnicas-avancadas.md) e [Checklists e templates](./28-checklists-e-templates.md).
