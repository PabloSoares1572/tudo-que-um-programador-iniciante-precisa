# 03 — Fundamentos: valores, variáveis e entrada

> 🟢 **Iniciante**

Uma variável é um nome que referencia um valor. Em Python, o tipo acompanha o valor e pode ser descoberto com `type()` durante o estudo.

```python
nome = "Ana"
idade = 20
altura = 1.65
estuda_python = True
sem_resposta = None
```

| Valor | Tipo | Uso comum |
| --- | --- | --- |
| `20` | `int` | números inteiros |
| `1.65` | `float` | números com parte decimal |
| `"Ana"` | `str` | texto |
| `True` / `False` | `bool` | condições |
| `None` | `NoneType` | ausência intencional de valor |

## Entrada e saída

`input()` sempre devolve texto. Converta antes de fazer conta:

```python
nome = input("Qual é seu nome? ")
idade = int(input("Qual é sua idade? "))
print(f"Olá, {nome}. No próximo ano você terá {idade + 1}.")
```

Se a pessoa digitar letras para `idade`, `int()` levantará `ValueError`. Por enquanto, aprenda a ler o erro; mais à frente você vai validar e tratar entradas.

## Conteúdos deste módulo

- [Strings](./01-strings.md)
- [Números e conversões](./02-numeros-e-conversoes.md)

← [Sintaxe](../02-Primeiro-Programa/01-sintaxe-indentacao-e-nomes.md) | [Operadores →](../04-Operadores/README.md)
