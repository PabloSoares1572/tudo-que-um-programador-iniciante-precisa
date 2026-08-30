# Coleções, cópias e valores padrão mutáveis

## Erro

Lista compartilhada inesperadamente, item removido durante loop ou \`AttributeError\` após usar retorno de \`.sort()\`.

## Por que acontece

Listas e dicionários são mutáveis; atribuição geralmente cria outra referência, não cópia. Métodos como \`.sort()\` alteram no local e retornam \`None\`.

## Exemplo incorreto

\`\`\`python
def adicionar(nome, nomes=[]):
    nomes.append(nome)
    return nomes
\`\`\`

A lista é criada uma vez e reutilizada entre chamadas.

## Como corrigir

\`\`\`python
def adicionar(nome, nomes=None):
    if nomes is None:
        nomes = []
    nomes.append(nome)
    return nomes
\`\`\`

## Como evitar

Use \`.copy()\`, slicing ou \`copy.deepcopy\` apenas quando entender a profundidade necessária. Ao percorrer coleção para remover itens, crie nova coleção ou itere sobre cópia.

