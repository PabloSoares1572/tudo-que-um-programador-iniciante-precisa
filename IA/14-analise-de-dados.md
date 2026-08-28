# 14 — IA para análise de dados

## Comece pela pergunta, não pelo gráfico

IA pode ajudar a limpar, explorar, explicar e visualizar dados. O valor vem de uma pergunta mensurável e de validação dos cálculos.

## Briefing mínimo

~~~text
Objetivo da análise: ...
Pergunta de negócio/estudo: ...
Fonte e período dos dados: ...
Dicionário de colunas: ...
Granularidade: uma linha representa ...
Métricas permitidas: ...
Formato desejado: tabela/gráfico/SQL/Python.
Restrições: não expor dados pessoais; indicar suposições.
~~~

## Processo seguro

1. Entenda cada coluna e unidade.
2. Verifique valores ausentes, duplicados e tipos.
3. Defina métricas e filtros antes de calcular.
4. Peça código ou fórmulas explicáveis.
5. Confira amostra manual e totalizadores.
6. Diferencie correlação de causalidade.
7. Documente dados, período e limitações.

## Exemplo de pedido

> Analise a planilha de vendas descrita abaixo. Primeiro, proponha uma checklist de qualidade dos dados. Depois, gere SQL PostgreSQL para receita mensal, ticket médio e clientes recorrentes. Explique cada query, use parâmetros quando aplicável e indique quais resultados precisariam de validação manual. Não invente colunas.

## Erros frequentes

| Erro | Como evitar |
| --- | --- |
| Somar colunas com unidades diferentes | Declare unidade e fórmula |
| Tratar texto como data ou número | Peça inspeção de tipos |
| Ignorar duplicidade | Defina chave única ou regra de deduplicação |
| Concluir causa a partir de correlação | Peça hipóteses e testes adicionais |
| Compartilhar dados sensíveis | Anonimize e use ambiente permitido |

## Gráficos que respondem perguntas

Peça primeiro: “qual gráfico melhor responde a esta pergunta e por quê?”. Em geral, linha mostra evolução no tempo; barras comparam categorias; dispersão mostra relação entre variáveis. O gráfico não substitui o número de origem.

## Prompt de revisão

> Revise esta análise como auditor de dados. Liste suposições, cálculos que devem ser reproduzidos, possíveis vieses de amostragem, campos ausentes e conclusões que excedem a evidência. Não reescreva os dados nem preencha lacunas com estimativas.

Consulte também [Pesquisa e verificação](./12-pesquisa-e-verificacao.md) e [Segurança e privacidade](./18-seguranca-e-privacidade.md).
