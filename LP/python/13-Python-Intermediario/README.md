# 13 — Python intermediário

> 🟡 **Intermediário**

Este módulo torna o código mais expressivo sem sacrificar clareza. O objetivo não é deixar tudo em uma linha; é escolher ferramentas que reduzem repetição e tornam a intenção visível.

## Comprehensions

Primeiro a versão explícita:

```python
quadrados = []
for numero in range(10):
    if numero % 2 == 0:
        quadrados.append(numero ** 2)
```

Depois a versão compacta, quando você já entende a anterior:

```python
quadrados = [numero ** 2 for numero in range(10) if numero % 2 == 0]
```

Comprehensions existem para listas, sets e dicionários. Se a expressão ficar difícil de ler, volte ao loop comum.

## Outros recursos

- [Iteráveis, iteradores, generators e decorators](./01-iteracao-generators-e-decorators.md)
- [Context managers, enums e collections](./02-context-managers-e-collections.md)

## Atividade

Transforme uma lista de nomes em uma lista de nomes normalizados (sem espaços nas pontas e em minúsculas), ignorando entradas vazias. Faça primeiro com `for`, depois compare com comprehension.

← [POO](../12-POO/README.md) | [Avançado →](../14-Python-Avancado/README.md)
