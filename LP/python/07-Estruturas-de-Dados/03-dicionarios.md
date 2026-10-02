# Dicionários

Um dicionário associa **chaves** a **valores**.

```python
usuario = {
    "nome": "Ana",
    "idade": 20,
}

usuario["idade"] = 21
print(usuario["nome"])
```

## Acesso seguro

`usuario["email"]` levanta `KeyError` se a chave não existir. Use `get` quando ausência for esperada:

```python
email = usuario.get("email")
```

## Iteração

```python
for chave, valor in usuario.items():
    print(chave, valor)
```

## Regras das chaves

Chaves devem ser únicas e imutáveis, como strings, números ou tuplas imutáveis. Uma lista não pode ser chave porque pode mudar.

## Atividade

Represente um produto com nome, preço e estoque. Atualize o estoque apenas se a quantidade solicitada for válida.

← [Tuplas](./02-tuplas.md) | [Sets →](./04-sets.md)
