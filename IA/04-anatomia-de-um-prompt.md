# 04 — Anatomia de um prompt excelente

## Template reutilizável

~~~text
[PAPEL]
Você é...

[OBJETIVO]
Sua tarefa é...

[CONTEXTO]
Estou trabalhando em...

[REQUISITOS]
- ...
- ...

[RESTRIÇÕES]
Não faça...

[FORMATO DA RESPOSTA]
Entregue...

[EXEMPLOS]
Entrada:
...
Saída esperada:
...
~~~

Use somente os blocos que ajudam. Um prompt de uma linha pode ser ótimo para tarefa simples; um briefing detalhado é útil quando a tarefa tem risco, regras ou muitas decisões.

## O que cada bloco resolve

| Bloco | Quando usar | Cuidado |
| --- | --- | --- |
| Papel | Para definir perspectiva ou experiência esperada | Não transforma a IA em autoridade real |
| Objetivo | Sempre que houver uma entrega clara | Escreva um verbo observável: comparar, revisar, criar |
| Contexto | Quando dados mudam a resposta | Evite informação irrelevante ou sensível |
| Requisitos | Para itens obrigatórios | Prefira lista curta e verificável |
| Restrições | Quando há limites importantes | Diga o que fazer em caso de dúvida |
| Formato | Quando a resposta será usada em outro lugar | Ex.: tabela, JSON válido, Markdown |
| Exemplos | Quando estilo ou classificação são difíceis | Use exemplos reais e consistentes |

## Exemplo completo

~~~text
[PAPEL]
Você é um revisor técnico.

[OBJETIVO]
Revise a descrição de uma API e encontre ambiguidades.

[CONTEXTO]
O público é uma equipe júnior que vai integrar um endpoint de pedidos.

[REQUISITOS]
- Liste ambiguidades por prioridade.
- Explique o impacto de cada uma.
- Sugira uma redação substituta.

[RESTRIÇÕES]
- Não invente endpoints ou campos que não estão no texto.
- Marque perguntas que precisam do responsável pelo produto.

[FORMATO]
Tabela: trecho | problema | impacto | sugestão.
~~~

## Prompt grande não é sinônimo de prompt bom

Um prompt enorme piora quando:

- mistura objetivos incompatíveis;
- repete a mesma instrução em palavras diferentes;
- traz documentos sem relação com a tarefa;
- esconde o pedido principal no meio de muitos detalhes.

Uma forma prática é começar curto e acrescentar contexto somente quando ele alterar a resposta.

## Teste de qualidade antes de enviar

1. A tarefa começa com um verbo claro?
2. A IA tem os dados necessários?
3. Há limites de tamanho, tom ou formato?
4. O resultado pode ser conferido?
5. Alguma informação sensível pode ser removida?

Veja também [Engenharia de prompt](./05-engenharia-de-prompt.md) e [Checklists e templates](./28-checklists-e-templates.md).
