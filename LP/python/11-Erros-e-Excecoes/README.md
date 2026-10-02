# 11 — Erros, exceções e tracebacks

> 🟡 **Intermediário inicial**

Erros não são sinal de incapacidade; eles são informação. A habilidade importante é ler o tipo, a mensagem e a linha do traceback.

## Tipos de problema

| Tipo | Exemplo |
| --- | --- |
| Sintaxe | esqueceu `:` ou fechou parêntese errado |
| Runtime/exception | tentou converter texto inválido com `int()` |
| Lógico | programa executa, mas calcula desconto errado |

## Tratamento específico

```python
texto = input("Idade: ")

try:
    idade = int(texto)
except ValueError:
    print("Digite uma idade inteira.")
else:
    print(f"Idade registrada: {idade}")
finally:
    print("Fim da tentativa.")
```

Capture apenas exceções esperadas e que você sabe tratar. Nunca use `except: pass` para esconder um problema.

## `raise`

Quando uma função detecta uma regra inválida, ela pode sinalizar claramente:

```python
def calcular_desconto(preco, percentual):
    if preco < 0 or not 0 <= percentual <= 100:
        raise ValueError("Preço ou percentual inválido")
    return preco * (1 - percentual / 100)
```

## Índice

- [Como ler tracebacks](./01-como-ler-tracebacks.md)
- [Estratégias de tratamento](./02-estrategias-de-tratamento.md)

← [Arquivos](../10-Arquivos/README.md) | [POO →](../12-POO/README.md)
