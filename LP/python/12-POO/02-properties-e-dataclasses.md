# Properties, métodos de classe e dataclasses

## `@property`

Use property quando um atributo precisa de validação ou cálculo, mas a interface de leitura deve continuar simples.

```python
class Temperatura:
    def __init__(self, celsius):
        self.celsius = celsius

    @property
    def fahrenheit(self):
        return self.celsius * 9 / 5 + 32
```

Não use property para esconder operações caras, chamadas de rede ou efeitos colaterais inesperados.

## `@classmethod` e `@staticmethod`

`@classmethod` recebe a classe e pode criar construtores alternativos. `@staticmethod` é uma função agrupada por contexto, sem `self` ou classe; não é obrigatório usá-la em todo helper.

## `dataclass`

Para classes principalmente de dados, `dataclasses` reduz repetição:

```python
from dataclasses import dataclass

@dataclass
class Produto:
    nome: str
    preco: float
```

Dataclass não substitui regras de domínio. Acrescente métodos e validações quando forem necessários.

← [Herança e composição](./01-heranca-e-composicao.md) | [Intermediário →](../13-Python-Intermediario/README.md)
