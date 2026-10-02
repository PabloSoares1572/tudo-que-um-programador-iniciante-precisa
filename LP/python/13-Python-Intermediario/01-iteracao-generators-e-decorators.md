# Iteração, generators e decorators

## Iterável x iterador

Uma lista é **iterável**: pode ser percorrida. Um **iterador** entrega itens um por vez e mantém estado. `iter()` obtém um iterador, e `next()` pede o próximo item.

```python
it = iter(["a", "b"])
print(next(it))
print(next(it))
```

Um `for` faz esse trabalho automaticamente e também termina corretamente ao fim.

## Generators

Um generator produz valores sob demanda com `yield`, útil para sequências grandes ou leitura incremental:

```python
def contar_ate(limite):
    for numero in range(1, limite + 1):
        yield numero
```

Não use generator só por moda. Se você precisa reutilizar a sequência várias vezes ou acessar posições, talvez uma lista seja mais adequada.

## Decorators

Decorators recebem uma função e devolvem outra função/objeto com comportamento adicional. São muito usados em frameworks, testes e logging, mas podem esconder fluxo. Primeiro entenda funções como objetos e closures; depois use decorators pequenos e documentados.

```python
def registrar(funcao):
    def interna(*args, **kwargs):
        print(f"Chamando {funcao.__name__}")
        return funcao(*args, **kwargs)
    return interna
```

Em código real, use `functools.wraps` ao criar decorators para preservar metadados da função original.

← [Intermediário](./README.md) | [Context managers →](./02-context-managers-e-collections.md)
