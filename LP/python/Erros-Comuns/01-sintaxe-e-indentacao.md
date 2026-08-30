# Sintaxe, \`:\` e indentação

## Erro

\`SyntaxError\` ou \`IndentationError\`.

## Por que acontece

Python exige dois-pontos após estruturas como \`if\`, \`for\`, \`while\`, \`def\` e \`class\`, e usa indentação para delimitar bloco.

## Exemplo incorreto

\`\`\`python
if idade >= 18
print("Maior")
\`\`\`

## Como corrigir

\`\`\`python
if idade >= 18:
    print("Maior")
\`\`\`

## Como evitar

Use quatro espaços por nível, configure o editor para não misturar tabs e leia a linha anterior à apontada: às vezes o erro é uma aspa/parêntese aberto antes dela.

