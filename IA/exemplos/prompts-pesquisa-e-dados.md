# Prompts para pesquisa e análise de dados

## 1. Planejar pesquisa

~~~text
Pergunta de pesquisa: [pergunta].
Escopo: [local, período, público].
Crie subperguntas, termos de busca, tipos de fonte prioritários e critérios de qualidade.
Não responda com fatos ainda; entregue somente um plano verificável.
~~~

## 2. Resumir fontes fornecidas

~~~text
Use somente as fontes abaixo.
Para cada fonte, extraia tese, evidências, data, limitações e citação curta identificadora.
Depois compare convergências e divergências. Não complete lacunas com conhecimento externo.

<fontes>
[fontes]
</fontes>
~~~

## 3. Checar afirmações

~~~text
Analise estas afirmações. Para cada uma, diga:
- que evidência seria necessária;
- qual tipo de fonte é mais apropriado;
- riscos de interpretação;
- se a frase precisa ser reescrita para não exagerar.
Não invente URL, artigo ou estatística.

[afirmações]
~~~

## 4. Criar dicionário de dados

~~~text
Com base no esquema abaixo, crie um dicionário de dados em tabela:
coluna, tipo esperado, significado, unidade, valores permitidos, valor ausente e observações.
Marque claramente campos cuja definição não está no esquema.

[esquema]
~~~

## 5. Explorar qualidade de dados

~~~text
Proponha um plano de qualidade para esta tabela: [tabela].
Inclua verificações de tipo, nulos, duplicidade, chaves, intervalos, consistência entre colunas e valores atípicos.
Entregue em SQL [dialeto] ou pseudocódigo, com explicação de cada teste.
~~~

## 6. Criar consulta SQL

~~~text
Banco: [dialeto]. Esquema: [tabelas e relações].
Pergunta: [pergunta].
Gere SQL e explique: filtros, joins, agregações, possíveis duplicações e índices a investigar.
Não invente colunas. Para campos ausentes, faça uma pergunta ou use comentário.
~~~

## 7. Interpretar resultado

~~~text
Estes são os resultados de uma análise: [resultados].
Separe observações diretas, hipóteses explicativas e informações insuficientes.
Sugira próximos testes para diferenciar as hipóteses. Não conclua causalidade apenas por correlação.
~~~

## 8. Sugerir gráfico

~~~text
Pergunta: [pergunta]. Dados: [colunas e período].
Sugira até 3 gráficos possíveis. Para cada um, explique o que responde, eixo, agregação, risco de interpretação e quando não usar.
~~~

## 9. Revisar análise

~~~text
Revise esta análise como auditor. Procure fórmula errada, filtro ausente, viés, duplicidade, período inconsistente e conclusão além da evidência.
Liste testes de reprodução e dados que faltam. Não altere números sem mostrar a regra.

[análise]
~~~

## 10. Produzir resumo com fontes

~~~text
Escreva síntese de até 400 palavras usando somente as fontes identificadas abaixo.
Coloque [Fonte A], [Fonte B] após cada afirmação relevante e inclua seção “Limitações e lacunas”.
Se uma fonte não sustentar a conclusão, não a use como prova.

[fontes]
~~~

Leia [Pesquisa e verificação](../12-pesquisa-e-verificacao.md) e [Análise de dados](../14-analise-de-dados.md).
