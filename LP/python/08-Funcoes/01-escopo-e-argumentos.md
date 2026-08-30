# Escopo, parâmetros e argumentos

## Escopo local

Variáveis criadas dentro de uma função normalmente só existem nela:

```python
def saudacao(nome):
    mensagem = f"Olá, {nome}"
    return mensagem
```

`mensagem` não deve ser usada fora da função. Isso reduz dependências escondidas.

## Argumentos posicionais e nomeados

```python
def apresentar(nome, cidade="São Paulo"):
    return f"{nome} mora em {cidade}."


apresentar("Ana")
apresentar(nome="Ana", cidade="Recife")
```

Valores padrão devem ser estáveis. Não use uma lista/dicionário mutável como valor padrão:

```python
def adicionar_item(item, itens=None):
    if itens is None:
        itens = []
    itens.append(item)
    return itens
```

## Global e nonlocal

Python possui `global` e `nonlocal`, mas eles aumentam o acoplamento e dificultam testes. Prefira receber dados por parâmetro e devolver o novo resultado.

## LEGB em termos simples

Ao procurar um nome, Python busca nos escopos **Local**, **Enclosing** (função externa), **Global** e **Built-in**. Você não precisa decorar a sigla agora; precisa evitar depender de estado global escondido.

← [Funções](./README.md) | [Funções avançadas →](./02-funcoes-avancadas.md)
