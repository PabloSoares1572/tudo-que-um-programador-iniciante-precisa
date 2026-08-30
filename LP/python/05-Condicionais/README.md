# 05 — Condicionais

> 🟢 **Iniciante**

Condicionais permitem que o programa escolha um caminho conforme uma condição.

```python
idade = 17

if idade >= 18:
    print("Maior de idade")
else:
    print("Menor de idade")
```

## Estrutura

```python
if condicao:
    # executa se a condição for verdadeira
    pass
elif outra_condicao:
    # executa se a primeira for falsa e esta for verdadeira
    pass
else:
    # executa nos demais casos
    pass
```

`elif` é opcional e pode aparecer mais de uma vez; `else` também é opcional. O `:` e a indentação fazem parte da sintaxe.

## Exemplo realista: classificação

```python
nota = float(input("Nota: "))

if nota < 0 or nota > 10:
    print("Nota inválida")
elif nota >= 7:
    print("Aprovado")
elif nota >= 5:
    print("Recuperação")
else:
    print("Reprovado")
```

## Boas práticas

- escreva condições simples e nomeie regras complexas;
- valide limites e dados antes de continuar;
- não use vários `if` independentes quando os casos são mutuamente exclusivos;
- trate uma condição por vez ao depurar.

## Atividade

Faça um programa que recebe preço e tipo de cliente (`normal` ou `vip`) e calcula desconto. Defina regras claras antes do código e teste valores inválidos.

← [Operadores](../04-Operadores/README.md) | [Padrões de validação →](./01-validacao-e-classificacao.md) | [Loops →](../06-Loops/README.md)
