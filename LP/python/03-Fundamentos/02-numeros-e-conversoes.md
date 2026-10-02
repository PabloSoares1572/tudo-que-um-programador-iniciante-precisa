# Números, conversões e `bool`

## Conversões explícitas

```python
quantidade = int("3")
preco = float("19.90")
texto = str(42)
```

Converter não “adivinha” formatos inválidos. `int("3.5")` falha; para esse texto, use `int(float("3.5"))` somente se a regra permitir arredondar para baixo — e deixe essa decisão explícita.

## Booleanos

`True` e `False` representam verdade lógica. Não compare com `== True` sem necessidade:

```python
ativo = True
if ativo:
    print("Conta ativa")
```

Alguns valores são considerados falsos em condições, como `0`, `""`, `[]`, `{}` e `None`. Use isso conscientemente; quando a regra de negócio precisa distinguir `0` de ausência, faça a checagem adequada.

## Cuidado com dinheiro

`float` usa representação binária e pode surpreender em valores monetários. Para aprender lógica, use `float`; em sistemas financeiros reais, estude `decimal.Decimal`, regras de arredondamento e valores em centavos inteiros.

## Atividade

Peça nome, idade e altura. Converta os valores necessários e mostre uma frase bem formatada. Teste com uma idade inválida para observar o traceback.

← [Strings](./01-strings.md) | [Operadores →](../04-Operadores/README.md)
