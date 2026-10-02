# Tipos avançados sem exagero

## Ferramentas úteis

| Recurso | Quando usar |
| --- | --- |
| `TypeAlias` | dar nome a tipo repetido e significativo |
| `Literal` | conjunto pequeno de valores literais válidos |
| `TypedDict` | formato de dicionário conhecido, como payload JSON |
| `Protocol` | comportamento esperado sem exigir herança |
| `Callable` | função que recebe/devolve tipos definidos |
| `TypeVar` / generics | preservar relação entre tipo de entrada e saída |

```python
from typing import TypedDict

class UsuarioPayload(TypedDict):
    nome: str
    ativo: bool
```

## Protocols

Um `Protocol` descreve capacidades. Por exemplo, algo que possui `salvar()` pode ser aceito por uma função sem estar preso a uma classe concreta. Isso reduz acoplamento quando realmente existe mais de uma implementação.

## Limite

Type hints ajudam desenvolvedores e ferramentas; dados de formulário, JSON ou banco ainda precisam ser validados. Uma anotação `idade: int` não torna automaticamente seguro um valor vindo de HTTP.

← [Type hints](./README.md) | [Testes →](../16-Testes/README.md)
