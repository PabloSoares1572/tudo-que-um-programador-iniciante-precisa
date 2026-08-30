# Exercícios — listas, dicionários e sets

## 🟢 1. Lista de compras

**Requisitos:** leia cinco itens, guarde em lista e imprima numerados.

## 🟡 2. Remover duplicados

**Requisitos:** dada uma lista de nomes, produza nomes únicos sem alterar a lista original. Explique se a ordem importa.

## 🟡 3. Produto em dicionário

**Requisitos:** crie um dicionário com nome, preço e estoque; reduza estoque apenas se houver quantidade suficiente.

## 🔴 4. Inventário resumido

**Requisitos:** receba uma lista de produtos, conte ocorrências e mostre os itens em ordem alfabética.

---

## Soluções de referência

### 1

\`\`\`python
itens = []
for indice in range(1, 6):
    itens.append(input(f"Item {indice}: ").strip())

for indice, item in enumerate(itens, start=1):
    print(f"{indice}. {item}")
\`\`\`

### 2

\`\`\`python
nomes = ["Ana", "João", "Ana", "Bia"]
unicos = list(dict.fromkeys(nomes))
print(unicos)
\`\`\`

\`set(nomes)\` remove duplicados, mas não deve ser usado se a ordem de apresentação for uma regra.

### 3

\`\`\`python
produto = {"nome": "Teclado", "preco": 120.0, "estoque": 3}
quantidade = 2

if 0 < quantidade <= produto["estoque"]:
    produto["estoque"] -= quantidade
    print("Venda registrada")
else:
    print("Quantidade inválida ou sem estoque")
\`\`\`

### 4

\`\`\`python
from collections import Counter

produtos = ["maçã", "café", "maçã", "leite"]
contagem = Counter(produtos)

for produto in sorted(contagem):
    print(f"{produto}: {contagem[produto]}")
\`\`\`

← [Controle](./02-controle-de-fluxo.md) | [Funções →](./04-funcoes.md)

