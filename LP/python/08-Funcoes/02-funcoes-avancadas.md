# Funções avançadas: `*args`, `**kwargs` e lambda

## Número variável de argumentos

```python
def somar(*numeros):
    return sum(numeros)


def mostrar_dados(**campos):
    for chave, valor in campos.items():
        print(f"{chave}: {valor}")
```

`*args` reúne argumentos posicionais extras em uma tupla; `**kwargs` reúne argumentos nomeados extras em um dicionário. Eles não são mágicos: escolha nomes mais descritivos quando a API for pública.

## Funções são objetos

Você pode guardar uma função em variável, passá-la para outra função ou devolvê-la. Esse conceito prepara decorators e callbacks, mas use com propósito — não para tornar código simples misterioso.

## `lambda`

Uma `lambda` é uma função curta de uma expressão:

```python
pares_ordenados = sorted(
    [("Ana", 20), ("João", 18)],
    key=lambda pessoa: pessoa[1],
)
```

Para lógica maior que uma expressão, use `def` e um nome claro.

## Exercício

Escreva uma função `calcular_total(*precos, desconto=0)` que soma preços e aplica desconto percentual. Crie testes manuais para lista vazia, um preço e desconto inválido.

← [Escopo](./01-escopo-e-argumentos.md) | [Módulos →](../09-Modulos-e-Pacotes/README.md)
