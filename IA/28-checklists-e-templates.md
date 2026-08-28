# 28 — Checklists e templates reutilizáveis

## Checklist antes de enviar um prompt

- [ ] O objetivo começa com verbo claro?
- [ ] Dei contexto que muda a resposta?
- [ ] Removi dado sensível e ruído?
- [ ] Informei formato, tamanho e público quando importa?
- [ ] Defini o que não pode acontecer?
- [ ] Sei como verificar o resultado?

## Template rápido

~~~text
Objetivo: [o que quero].
Contexto: [dados que alteram a resposta].
Requisitos: [itens obrigatórios].
Restrições: [limites e o que evitar].
Formato: [como entregar].
Se faltar informação: [pergunte / marque como não informado].
~~~

## Template para pesquisa

~~~text
Pergunta: [pergunta].
Escopo: [lugar, período, público].
Priorize: [fontes oficiais/primárias/independentes].
Entregue: plano de busca, fontes a verificar e critérios de evidência.
Não invente links ou dados. Separe fato, inferência e lacuna.
~~~

## Template para programação

~~~text
Objetivo: [funcionalidade/correção].
Stack e versões: [tecnologias].
Contexto: [arquivos/erro/comportamento atual].
Regras: [negócio e compatibilidade].
Critérios de aceitação: [testes/resultados].
Antes de editar: leia arquivos relevantes e apresente plano.
Depois: informe diff, testes executados e riscos.
Não acesse segredos nem altere fora do escopo.
~~~

## Template para revisão de texto

~~~text
Público: [quem lê].
Objetivo: [efeito esperado].
Tom: [tom].
Limite: [tamanho].
Revise clareza, estrutura, repetição e fatos não sustentados.
Preserve a intenção. Mostre primeiro os principais ajustes e depois a versão final.
~~~

## Template para análise de dados

~~~text
Pergunta: [pergunta].
Dados disponíveis: [colunas, período, granularidade].
Métricas: [fórmulas permitidas].
Entregue: [SQL/Python/tabela/gráfico].
Indique suposições, dados faltantes e como reproduzir cálculos.
Não inferir causalidade sem evidência.
~~~

## Checklist de validação final

- [ ] Fatos importantes têm fonte ou estão marcados como hipótese.
- [ ] Cálculos e código foram executados/checados.
- [ ] Formato pode ser consumido pelo destino.
- [ ] Não há dados secretos, pessoais ou confidenciais expostos.
- [ ] Ação externa ainda precisa de aprovação humana?
- [ ] O resultado cumpre os critérios de aceitação?

Use a [biblioteca de prompts](./README.md#biblioteca-de-prompts) como ponto de partida e adapte sempre ao caso real.
