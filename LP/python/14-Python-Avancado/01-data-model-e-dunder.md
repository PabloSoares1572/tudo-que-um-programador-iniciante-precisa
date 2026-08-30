# Data model e métodos especiais

Métodos especiais, também chamados de **dunder methods**, definem como objetos interagem com operadores e funções da linguagem. Eles têm nomes como `__init__`, `__repr__`, `__len__` e `__eq__`.

```python
class Carrinho:
    def __init__(self, itens):
        self.itens = list(itens)

    def __len__(self):
        return len(self.itens)

    def __repr__(self):
        return f"Carrinho(itens={self.itens!r})"
```

Agora `len(carrinho)` e uma representação útil no debugger funcionam naturalmente.

## Regras importantes

- implemente apenas o comportamento que faz sentido;
- mantenha `__repr__` útil para desenvolvedores;
- respeite contratos: se define igualdade, pense em hash e imutabilidade;
- não esconda I/O, rede ou alteração de banco dentro de métodos aparentemente simples como `__len__` ou `__str__`.

## Descriptors e metaclasses

Descriptors são objetos que controlam acesso a atributos; `property` usa esse mecanismo. Metaclasses controlam criação de classes. São poderosos, mas frameworks geralmente já os usam por você. Aprenda para entender ferramentas e resolver necessidade real, não para decorar.

← [Avançado](./README.md) | [CPython e GIL →](./02-cpython-memoria-e-gil.md)
