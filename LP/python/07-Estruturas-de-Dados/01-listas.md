# Listas

Listas guardam uma sequência mutável de valores.

```python
tarefas = ["estudar", "praticar"]
tarefas.append("revisar")
primeira = tarefas[0]
```

## Operações frequentes

```python
numeros = [3, 1, 2]
numeros.append(4)
numeros.remove(1)
ordenados = sorted(numeros)
copia = numeros.copy()
```

`sorted(numeros)` cria outra lista; `numeros.sort()` altera a lista existente e retorna `None`. Observe a diferença para não escrever `numeros = numeros.sort()`.

## Percorrendo

```python
for tarefa in tarefas:
    print(tarefa)
```

Se precisar de índice e valor, use `enumerate(tarefas, start=1)`.

## Slicing e cópia

`valores[:]` cria uma cópia superficial. Listas dentro de listas continuam sendo compartilhadas; estruturas aninhadas exigem mais atenção.

## Atividade

Crie uma lista de compras. Permita adicionar três itens e mostre-os numerados sem modificar a lista durante a iteração.

← [Estruturas](./README.md) | [Tuplas →](./02-tuplas.md)
