# `range`, laços aninhados e erros de repetição

## `range` em três formas

```python
range(5)         # 0 até 4
range(2, 5)      # 2 até 4
range(0, 10, 2)  # 0, 2, 4, 6, 8
```

Para contar para trás, o passo precisa ser negativo:

```python
for numero in range(5, 0, -1):
    print(numero)
```

## Laços aninhados

Um loop dentro de outro é válido para tabelas, matrizes e combinações, mas o trabalho cresce rápido. Comece com entradas pequenas e nomes claros.

```python
for linha in range(1, 4):
    for coluna in range(1, 4):
        print(f"({linha}, {coluna})")
```

## `else` em loops

Um loop pode ter `else`, executado quando ele termina sem `break`. É um recurso válido, mas, no início, prefira uma variável booleana ou uma função para manter a intenção evidente.

## Erros comuns

- alterar a variável de controle de modo errado no `while`;
- usar `range` esperando que o limite final entre na sequência;
- modificar uma lista enquanto itera sobre ela;
- usar loop quando uma função pronta ou operação de coleção seria mais clara.

← [Loops](./README.md) | [Estruturas de dados →](../07-Estruturas-de-Dados/README.md)
