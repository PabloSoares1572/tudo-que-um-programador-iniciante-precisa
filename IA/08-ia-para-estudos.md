# 08 — IA para estudos: aprender, não só copiar

## O melhor uso: tutor ativo

IA pode explicar um conceito em níveis diferentes, criar exercícios e apontar lacunas. Ela vira uma muleta quando entrega respostas prontas que você não tenta entender. O objetivo é sair da conversa sabendo resolver uma questão sem ajuda.

## Ciclo de estudo com IA

1. Defina o assunto e o resultado esperado.
2. Peça uma explicação curta com exemplo.
3. Tente resolver um exercício sozinho.
4. Peça correção com foco no seu erro.
5. Faça uma variação do exercício sem consultar a resposta.
6. Revise depois com flashcards ou perguntas.

## Prompt para explicação adaptativa

~~~text
Atue como tutor de [assunto]. Meu nível atual é [iniciante/intermediário].
Explique [conceito] em até 250 palavras, sem assumir conhecimentos que eu não citei.
Use uma analogia curta e um exemplo resolvido.
Depois crie 3 exercícios progressivos sem gabarito.
Só mostre a resposta de cada exercício quando eu tentar.
~~~

## Prompt ruim x melhorado

❌ “Me ensine normalização de banco de dados.”

✅ “Explique 1FN, 2FN e 3FN para alguém que sabe criar tabelas SQL, mas nunca estudou normalização. Use uma tabela de pedidos como exemplo. Mostre um caso com redundância, decomponha passo a passo e crie quatro exercícios. Não avance para BCNF ainda.”

## Usos úteis

| Objetivo | Como pedir |
| --- | --- |
| Resumo | “Resuma por tópicos, destaque definições e dúvidas possíveis” |
| Exercícios | “Crie 10 questões em ordem de dificuldade, com gabarito separado” |
| Flashcards | “Crie cartões pergunta → resposta curta em CSV” |
| Simulado | “Monte prova com tempo, critérios e comentários após minhas respostas” |
| Revisão | “Compare minha resposta com a rubrica e diga o que falta” |
| Plano | “Distribua os tópicos conforme prazo e tempo diário realista” |

## Transforme erro em aprendizado

Em vez de pedir a resposta imediatamente:

> Esta foi minha tentativa: [resposta]. Não resolva ainda. Identifique o primeiro conceito que apliquei errado, faça uma pergunta-guia e espere minha nova tentativa.

Esse método fortalece raciocínio e evita a ilusão de aprendizado gerada por leitura passiva.

## Cuidado com fontes

Para conteúdos de prova, leis, medicina, ciência ou tecnologia que muda rápido, use o material oficial como fonte principal. Peça à IA para explicar o conteúdo que você forneceu e confira citações antes de estudar algo como fato.

## Mini-rotina de 30 minutos

- 5 min: objetivo e diagnóstico rápido.
- 10 min: explicação com exemplo.
- 10 min: dois exercícios sem ajuda.
- 5 min: correção e flashcards do erro.

Biblioteca: [prompts para estudos](./exemplos/prompts-estudos.md). Para aprender a pedir melhor, volte a [Como conversar com IA](./03-conversar-com-ia.md).
