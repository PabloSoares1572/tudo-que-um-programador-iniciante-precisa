# Exercícios — funções

## 🟢 1. Área de retângulo

**Requisitos:** crie \`calcular_area(largura, altura)\` que devolve a área.

## 🟡 2. Validador de faixa

**Requisitos:** crie \`esta_na_faixa(valor, minimo, maximo)\` que devolve booleano.

## 🟡 3. Média com validação

**Requisitos:** função recebe notas; recuse lista vazia e nota fora de 0–10 com \`ValueError\`.

## 🔴 4. Carrinho

**Requisitos:** crie função que recebe preços variáveis e desconto opcional; não aceite preço negativo ou desconto fora de 0–100.

---

## Soluções de referência

### 1 e 2

\`\`\`python
def calcular_area(largura, altura):
    return largura * altura


def esta_na_faixa(valor, minimo, maximo):
    return minimo <= valor <= maximo
\`\`\`

### 3

\`\`\`python
def calcular_media(notas):
    if not notas:
        raise ValueError("Informe ao menos uma nota")
    if any(nota < 0 or nota > 10 for nota in notas):
        raise ValueError("Notas devem estar entre 0 e 10")
    return sum(notas) / len(notas)
\`\`\`

### 4

\`\`\`python
def calcular_total(*precos, desconto=0):
    if any(preco < 0 for preco in precos):
        raise ValueError("Preço negativo")
    if not 0 <= desconto <= 100:
        raise ValueError("Desconto inválido")
    subtotal = sum(precos)
    return subtotal * (1 - desconto / 100)
\`\`\`

Crie testes manuais para cada erro. Depois transforme-os em pytest no próximo módulo.

← [Coleções](./03-colecoes.md) | [Arquivos e exceções →](./05-arquivos-e-excecoes.md)

