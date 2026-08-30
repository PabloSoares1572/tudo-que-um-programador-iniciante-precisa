# Herança, composição e polimorfismo

## Herança

Herança representa uma relação “é um tipo de”. Por exemplo, uma `ContaPoupanca` pode ser uma conta com regra adicional. Use apenas quando a relação for verdadeira e o contrato da classe base continuar válido.

## Composição

Composição representa “tem um”. Uma `Pedido` tem uma lista de itens; um `ServicoEmail` pode receber uma configuração. Na prática, composição costuma reduzir acoplamento e tornar testes mais simples.

```python
class Item:
    def __init__(self, nome, preco):
        self.nome = nome
        self.preco = preco


class Pedido:
    def __init__(self, itens):
        self.itens = list(itens)

    def total(self):
        return sum(item.preco for item in self.itens)
```

## Polimorfismo

É tratar objetos diferentes por uma interface comum. Antes de criar uma hierarquia profunda, verifique se basta uma função, um protocolo ou composição.

← [POO](./README.md) | [Dataclasses →](./02-properties-e-dataclasses.md)
