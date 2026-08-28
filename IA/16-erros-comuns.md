# 16 — Erros comuns ao usar IA

## Diagnóstico rápido

Se a resposta parece genérica, errada ou fora do formato, normalmente falta contexto, critérios de aceitação, uma fonte confiável ou uma etapa de verificação.

| Erro | Sintoma | Correção |
| --- | --- | --- |
| Pedido vago | Resposta genérica | Declare objetivo, público e formato |
| Contexto demais | IA ignora o essencial | Remova informação que não altera a tarefa |
| Muitas tarefas juntas | Parte da resposta fica incompleta | Quebre em etapas |
| Sem formato | Resultado difícil de usar | Peça tabela, checklist, JSON ou estrutura |
| Confiar em tudo | Fatos e citações incorretos passam | Verifique fontes e testes |
| Sem feedback | Repetição do mesmo erro | Diga exatamente o que mudar |
| Usar dado secreto | Risco de vazamento | Anonimize ou não envie |
| Automatizar sem revisão | Ação errada ganha escala | Exija aprovação e logs |

## Exemplos

❌ “Faça melhor.”

✅ “Mantenha os fatos, reduza para 120 palavras, use tom informal e finalize com uma checklist de quatro itens.”

❌ “Me dê fontes sobre isso.”

✅ “Liste fontes oficiais ou primárias que eu deveria consultar para verificar esta afirmação. Não invente links; se não puder pesquisar, diga que preciso buscar externamente.”

❌ “Corrija meu código.”

✅ “Este é o erro, este é o trecho mínimo e este é o comportamento esperado. Primeiro explique a hipótese, depois sugira patch pequeno e testes.”

## Evite antropomorfizar

Falar “a IA entendeu” pode ser prático, mas não significa que ela possui intenção ou memória humana. Pergunte o que ela assumiu, valide e ajuste a entrada.

## Quando parar de insistir no prompt

Troque de estratégia se:

- falta uma fonte, arquivo ou dado essencial;
- o cálculo precisa ser reproduzido por ferramenta exata;
- a tarefa exige autorização humana;
- a resposta depende de informação atual que não foi pesquisada;
- o modelo erra repetidamente no mesmo ponto.

Uma boa pergunta pode ser: “qual dado ou ferramenta está faltando para fazer isso com segurança?”.

Leia [Limitações e alucinações](./17-limitacoes-e-alucinacoes.md) e [Contexto e instruções](./07-contexto-e-instrucoes.md).
