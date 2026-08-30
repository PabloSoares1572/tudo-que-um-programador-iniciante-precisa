# 15 — Type hints

> 🟡 **Intermediário → 🔴 Avançado**

Type hints documentam os tipos esperados e permitem que ferramentas encontrem erros antes da execução. Python continua dinamicamente tipado em runtime na maior parte dos casos: a anotação não converte nem bloqueia automaticamente valores.

```python
def somar(a: int, b: int) -> int:
    return a + b
```

## Sintaxe moderna

```python
def buscar_usuario(usuario_id: int) -> dict[str, str] | None:
    ...
```

Use `T | None` para algo que pode estar ausente, quando a versão mínima do projeto permitir. Para compatibilidade ou tipos mais complexos, consulte `typing`.

## Por que usar?

- deixa contratos de funções mais claros;
- ajuda IDEs e verificadores como mypy/pyright;
- melhora refatorações;
- não substitui validação de entrada externa.

## Ordem certa

Primeiro escreva função compreensível, cubra comportamento com testes e, então, acrescente tipos úteis. Não anote cada detalhe sem entender o contrato.

## Próximo

- [Tipos avançados](./01-tipos-avancados.md)

← [Python avançado](../14-Python-Avancado/README.md) | [Testes →](../16-Testes/README.md)
