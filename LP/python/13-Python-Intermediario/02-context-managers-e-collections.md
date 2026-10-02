# Context managers, enums e collections

## Context managers

`with` usa um context manager para preparar e liberar recursos de forma segura. Arquivos são o exemplo clássico; conexões e locks também podem usar esse padrão.

```python
with open("dados.txt", encoding="utf-8") as arquivo:
    conteudo = arquivo.read()
```

## `Enum`

Use enum para conjunto fechado de valores nomeados, em vez de strings soltas repetidas pelo projeto.

```python
from enum import Enum

class StatusPedido(Enum):
    PENDENTE = "pendente"
    PAGO = "pago"
```

## `collections`

- `Counter`: contagem de itens;
- `defaultdict`: valor padrão por chave;
- `deque`: fila eficiente nas extremidades;
- `namedtuple`: estrutura leve nomeada, hoje muitas vezes substituída por dataclass.

Escolha a estrutura pelo problema. Uma lista não deve virar `deque` sem que haja operação frequente na frente, por exemplo.

← [Iteração](./01-iteracao-generators-e-decorators.md) | [Avançado →](../14-Python-Avancado/README.md)
