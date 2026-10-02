# Funções

\`\`\`python
def calcular_total(preco, quantidade=1):
    return preco * quantidade

def somar(*numeros):
    return sum(numeros)

def mostrar(**campos):
    return campos
\`\`\`

- Parâmetro: nome na definição; argumento: valor na chamada.
- \`return\` devolve resultado; sem ele, função devolve \`None\`.
- Prefira função pura para regras de negócio.
- Não use coleção mutável como valor padrão; use \`None\`.

