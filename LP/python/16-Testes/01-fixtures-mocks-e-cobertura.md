# Fixtures, mocks e cobertura

## Fixtures

Fixtures preparam dados ou recursos reutilizáveis para testes. Em pytest, elas ajudam a evitar repetição e deixar o estado de teste explícito.

## Mocks

Mock substitui uma dependência externa — como API, e-mail ou relógio — para que o teste seja determinístico. Não use mocks para testar a implementação interna sem necessidade; teste o contrato observável.

## Cobertura

Cobertura mede quais linhas/caminhos foram executados pelos testes. 100% não garante qualidade; testes podem passar sem verificar comportamento relevante. Use cobertura como sinal para encontrar áreas esquecidas, não como único objetivo.

## Exemplo de erro esperado

```python
import pytest

def dividir(a, b):
    if b == 0:
        raise ValueError("Divisor não pode ser zero")
    return a / b


def test_dividir_por_zero():
    with pytest.raises(ValueError, match="Divisor"):
        dividir(1, 0)
```

← [Testes](./README.md) | [Estratégia →](./02-estrategia-de-testes.md)
