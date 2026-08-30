# Comparação, tipos e \`input()\`

## Erro

Confundir \`=\` com \`==\`, ou receber \`TypeError\`/\`ValueError\` após usar \`input()\`.

## Por que acontece

\`=\` atribui; \`==\` compara. Além disso, \`input()\` sempre devolve \`str\`.

## Exemplo incorreto

\`\`\`python
idade = input("Idade: ")
if idade >= 18:
    print("Maior")
\`\`\`

## Como corrigir

\`\`\`python
idade = int(input("Idade: "))
if idade >= 18:
    print("Maior")
\`\`\`

## Como evitar

Antes de operar, pergunte: “qual tipo chega aqui?”. Teste entrada vazia e texto inválido. Para dados externos, valide/trate em vez de confiar na conversão.

