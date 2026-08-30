# 08 — Funções

> 🟢 **Iniciante → 🟡 Intermediário**

Funções dividem um problema em partes reutilizáveis e testáveis.

```python
def calcular_media(nota_1, nota_2):
    return (nota_1 + nota_2) / 2


media = calcular_media(7.0, 9.0)
print(media)
```

## Linha por linha

- `def` inicia a definição.
- `calcular_media` é o nome da função.
- `nota_1` e `nota_2` são parâmetros.
- `return` devolve o resultado e encerra a função.
- `7.0` e `9.0` são argumentos da chamada.

Evite uma função que faz leitura de entrada, cálculo, impressão, arquivo e rede ao mesmo tempo. Funções pequenas, com responsabilidade clara, são mais fáceis de entender e testar.

## Índice

- [Escopo e argumentos](./01-escopo-e-argumentos.md)
- [Funções avançadas](./02-funcoes-avancadas.md)

## Atividade

Crie `eh_par(numero)` que devolve `True` para pares e `False` para ímpares. Não imprima dentro da função; imprima apenas fora dela para testar o retorno.

← [Estruturas](../07-Estruturas-de-Dados/README.md) | [Módulos →](../09-Modulos-e-Pacotes/README.md)
