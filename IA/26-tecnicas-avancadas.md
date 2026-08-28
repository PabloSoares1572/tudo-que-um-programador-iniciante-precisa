# 26 — Técnicas avançadas para melhorar resultados

## Melhoria sistemática, não tentativa aleatória

Técnicas avançadas são úteis quando a tarefa é repetida, complexa ou tem custo de erro. O foco é estabelecer processo, critérios e avaliação.

## 1. Decomposição com contratos

Quebre tarefa em etapas e defina a saída esperada de cada uma. Exemplo: pesquisa → fatos com fontes → outline → rascunho → revisão. Uma etapa não deve inventar dados que cabem à anterior.

## 2. Rubricas de qualidade

Crie critérios objetivos antes da geração:

| Critério | Pergunta |
| --- | --- |
| Correção | É sustentado por dado, teste ou fonte? |
| Completude | Cobre todos os requisitos? |
| Clareza | O público consegue usar? |
| Segurança | Expõe dados ou sugere ação perigosa? |
| Formato | Está pronto para o destino? |

## 3. Casos de teste para prompts

Não avalie um prompt em um único exemplo. Teste caso comum, limite, dado ausente, instrução ambígua, conteúdo adversarial e formato inválido. Registre versão do prompt, modelo, entrada, saída e resultado.

## 4. Contexto recuperado

Para documentos grandes, use busca/RAG em vez de colar tudo sem ordem. Traga trechos relevantes com origem e peça citações. Isso reduz ruído e facilita auditoria.

## 5. Comparação de alternativas

> Para cada alternativa, indique hipótese, evidência necessária, custo, risco, dependências e primeiro experimento. Não trate a lista como recomendação final.

## 6. Revisão independente

Peça um segundo passe com outra função: autor, revisor técnico, verificador de requisitos e leitor do público. Mesmo assim, valide externamente itens críticos; dois textos de IA podem repetir o mesmo erro.

## 7. Human-in-the-loop

Defina pontos de aprovação antes de ações externas. Isso é especialmente importante em mensagens, dados, código, finanças e mudanças de produção.

## 8. Versão e observabilidade

Para fluxos de produção, guarde versão do prompt, configuração, fonte de contexto, métrica e feedback humano. Sem isso, não é possível explicar por que a qualidade mudou.

## Quando não avançar

Não crie agente, RAG ou pipeline sofisticado para uma tarefa rara que um prompt curto e revisão manual resolvem. Complexidade também cria custo, falhas e riscos.

Leia [Prompts avançados](./15-prompts-avancados.md), [RAG](./21-rag-e-bases-de-conhecimento.md) e [Automações](./22-automacoes-com-ia.md).
