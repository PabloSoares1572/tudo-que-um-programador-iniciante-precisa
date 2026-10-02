# 04 — Operadores

> 🟢 **Iniciante**

Operadores combinam ou comparam valores.

## Aritméticos

```python
total = 10 + 3      # 13
diferenca = 10 - 3  # 7
produto = 10 * 3    # 30
divisao = 10 / 3    # 3.333...
inteira = 10 // 3   # 3
resto = 10 % 3      # 1
potencia = 2 ** 3   # 8
```

## Comparação e lógica

```python
idade = 20
maior = idade >= 18
tem_documento = True
pode_entrar = maior and tem_documento
```

Comparações usam `==`, `!=`, `>`, `<`, `>=` e `<=`. `=` atribui um valor; `==` compara. Confundir os dois é um erro frequente para iniciantes.

## Atribuição composta

```python
contador = 0
contador += 1
```

## Precedência

Python segue regras de precedência, mas parênteses deixam a intenção clara:

```python
media = (nota_1 + nota_2) / 2
```

Evite expressões enormes. Nomeie partes intermediárias se isso tornar a regra mais fácil de testar.

## Exercício

Calcule o preço final a partir de preço, quantidade e desconto percentual. Mostre o resultado com duas casas decimais e teste com desconto zero, 10 e 100.

← [Fundamentos](../03-Fundamentos/README.md) | [Condicionais →](../05-Condicionais/README.md)
