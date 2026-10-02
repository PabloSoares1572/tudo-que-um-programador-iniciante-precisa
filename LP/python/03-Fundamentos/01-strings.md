# Strings: texto em Python

Strings são sequências imutáveis de caracteres. Você pode usar aspas simples ou duplas, desde que abra e feche com o mesmo tipo.

```python
mensagem = "Python é prático"
primeira_letra = mensagem[0]
parte = mensagem[0:6]
```

Índices começam em zero. `mensagem[0]` é `P`; `mensagem[0:6]` pega do início até antes do índice 6.

## Métodos úteis

```python
nome = "  Pablo  "
limpo = nome.strip()
maiusculo = limpo.upper()
tem_letra_a = "a" in limpo.lower()
```

Strings não mudam “por dentro”; métodos normalmente devolvem uma nova string. Por isso `nome.strip()` não altera `nome` se você não guardar ou usar o resultado.

## Formatação com f-string

```python
produto = "teclado"
preco = 120.0
print(f"{produto}: R$ {preco:.2f}")
```

F-strings são claras para inserir valores. Não use concatenação confusa quando uma f-string deixa a intenção mais evidente.

## Erros comuns

- acessar índice fora do tamanho: `IndexError`;
- esquecer que `input()` já é string;
- tentar alterar um caractere por índice em uma string;
- misturar aspas sem escapar o caractere necessário.

← [Fundamentos](./README.md) | [Números e conversões →](./02-numeros-e-conversoes.md)
