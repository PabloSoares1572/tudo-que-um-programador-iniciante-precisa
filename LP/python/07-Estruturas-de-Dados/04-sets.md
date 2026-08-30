# Sets (conjuntos)

Sets guardam elementos únicos. São úteis para remover duplicados e comparar grupos.

```python
linguagens = {"Python", "Java", "Python"}
print(linguagens)  # contém Python apenas uma vez
```

## Operações de conjunto

```python
backend = {"Python", "SQL", "HTTP"}
dados = {"Python", "SQL", "Pandas"}

comuns = backend & dados
todos = backend | dados
somente_backend = backend - dados
```

Não use a ordem de um `set` como parte da regra do seu programa. Se precisar de apresentação ordenada, use `sorted(...)` no momento de mostrar o resultado.

## Caso de uso

Para verificar se há itens repetidos em uma lista:

```python
itens = ["a", "b", "a"]
tem_repetidos = len(itens) != len(set(itens))
```

← [Dicionários](./03-dicionarios.md) | [Funções →](../08-Funcoes/README.md)
