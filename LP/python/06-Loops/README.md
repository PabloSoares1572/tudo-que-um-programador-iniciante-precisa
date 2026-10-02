# 06 — Loops e repetição

> 🟢 **Iniciante**

Loops repetem uma ação. Use `for` quando sabe sobre quais itens ou intervalo vai iterar; use `while` quando a repetição depende de uma condição que muda.

## `for` com `range`

```python
for numero in range(1, 6):
    print(numero)
```

O fim de `range(1, 6)` não é incluído: imprime de 1 a 5.

## `while`

```python
tentativas = 0

while tentativas < 3:
    print("Tentativa", tentativas + 1)
    tentativas += 1
```

Em um `while`, identifique sempre qual variável fará a condição ficar falsa. Sem isso, você cria um loop infinito.

## `break` e `continue`

- `break` encerra o loop atual;
- `continue` pula para a próxima repetição.

Use-os com parcimônia; às vezes reorganizar a condição torna o código mais claro.

## Exemplo: soma validada

```python
total = 0

for texto in ["10", "20", "invalido", "5"]:
    if not texto.isdigit():
        continue
    total += int(texto)

print(total)
```

## Atividade

Faça uma tabuada de um número escolhido pelo usuário, de 1 a 10. Em seguida, crie um jogo que permite até três tentativas para acertar uma senha fictícia.

← [Condicionais](../05-Condicionais/README.md) | [Detalhes de loops →](./01-range-break-continue.md) | [Estruturas de dados →](../07-Estruturas-de-Dados/README.md)
