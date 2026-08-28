# 05 — Engenharia de prompt

## O que é

Engenharia de prompt é o processo de projetar, testar e melhorar instruções para obter resultados úteis e confiáveis de um modelo. Não é decorar “palavras mágicas”. É transformar uma necessidade real em uma especificação clara.

## Processo recomendado

1. Defina a decisão ou entrega final.
2. Liste dados disponíveis e lacunas.
3. Escolha o formato de saída.
4. Escreva a primeira versão do prompt.
5. Teste com casos fáceis e casos extremos.
6. Avalie contra critérios objetivos.
7. Ajuste uma coisa por vez e registre o que funcionou.

## Técnicas principais

| Técnica | O que faz | Melhor uso |
| --- | --- | --- |
| Zero-shot | Dá só a instrução | Tarefas diretas e comuns |
| One-shot | Dá um exemplo | Quando o formato é novo |
| Few-shot | Dá alguns exemplos | Classificação e estilo consistente |
| Role prompting | Define perspectiva | Revisão, tutoria, planejamento |
| Context prompting | Entrega informações relevantes | Tarefas ligadas a um projeto ou documento |
| Constraint prompting | Define limites claros | Segurança, tamanho, escopo e tom |
| Structured prompting | Pede uma estrutura | Tabelas, Markdown e JSON |
| Decomposition | Quebra uma tarefa grande | Projetos com várias etapas |
| Chaining | Usa uma saída como insumo da próxima etapa | Pesquisa, escrita e revisão |
| Refinement | Melhora uma versão existente | Edição e controle de qualidade |

## Zero-shot x few-shot

❌ **Zero-shot insuficiente**

> Classifique este comentário como positivo, neutro ou negativo.

✅ **Few-shot com padrão**

~~~text
Classifique cada comentário como positivo, neutro ou negativo.

Exemplos:
“Entrega rápida e produto ótimo.” → positivo
“O produto chegou hoje.” → neutro
“Veio incompleto e atrasado.” → negativo

Agora classifique: “O suporte resolveu meu problema depois de dois dias.”
Responda somente com uma das três categorias.
~~~

Os exemplos deixam explícita a regra de classificação e o formato.

## Saída estruturada

Se uma resposta será lida por sistema, peça uma estrutura verificável.

~~~text
Extraia as tarefas do texto abaixo.
Retorne JSON válido com a estrutura:
{
  "tarefas": [{"titulo": "", "prazo": null, "responsavel": null}]
}
Não inclua texto antes ou depois do JSON. Use null quando a informação não existir.
~~~

Depois valide o JSON no seu código. Nunca presuma que texto gerado automaticamente está perfeito.

## Critérios de avaliação

Acrescente critérios quando a qualidade importa:

> Avalie a resposta em clareza, correção, completude e aderência ao público. Dê uma nota de 0 a 2 para cada critério, explique brevemente e reescreva apenas se a soma for menor que 7.

Use isso como apoio de revisão, não como prova de que o modelo está certo.

Continue em [Técnicas de prompt](./06-tecnicas-de-prompt.md).
