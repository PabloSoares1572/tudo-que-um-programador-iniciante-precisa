# 16 — Testes automatizados

> 🟡 **Intermediário → ⚫ Profissional**

Testes verificam comportamento esperado de forma repetível. Eles não provam que não existe bug, mas reduzem regressões e deixam mudanças mais seguras.

## Pirâmide prática

- **unitário:** testa uma função/classe pequena e rápida;
- **integração:** verifica componentes trabalhando juntos;
- **fim a fim:** testa fluxo real, geralmente mais lento e caro.

## Primeiro teste com `pytest`

```python
def somar(a, b):
    return a + b


def test_somar_dois_inteiros():
    assert somar(2, 3) == 5
```

Instale `pytest` dentro do ambiente virtual e execute `python -m pytest`. Use `python -m` para garantir que o pytest pertence ao mesmo interpretador/ambiente do projeto.

## O que testar?

- caso normal;
- limites: zero, vazio, mínimo, máximo;
- entradas inválidas e exceções esperadas;
- regressões de bugs corrigidos.

## Índice

- [Fixtures, mocks e cobertura](./01-fixtures-mocks-e-cobertura.md)
- [Testar projetos](./02-estrategia-de-testes.md)

← [Type hints](../15-Type-Hints/README.md) | [Debugging →](../17-Debugging/README.md)
