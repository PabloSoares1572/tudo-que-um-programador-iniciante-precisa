# 12 — Programação orientada a objetos (POO)

> 🟡 **Intermediário**

POO é uma forma de organizar código que junta **dados** e **comportamentos** relacionados. Não é requisito para todo problema; funções e estruturas simples muitas vezes são melhores.

```python
class Conta:
    def __init__(self, titular, saldo=0.0):
        self.titular = titular
        self.saldo = saldo

    def depositar(self, valor):
        if valor <= 0:
            raise ValueError("O depósito deve ser positivo")
        self.saldo += valor


conta = Conta("Ana")
conta.depositar(100)
```

## Termos

- **classe:** molde, como `Conta`;
- **instância/objeto:** uma conta concreta criada a partir da classe;
- **atributo:** dado da instância, como `saldo`;
- **método:** função da classe, como `depositar`;
- **`self`:** referência à instância que recebeu a chamada.

## Princípios úteis

Encapsule regras importantes no objeto; prefira composição a herança quando objetos colaboram; não crie classe apenas para guardar uma função. Uma boa classe tem uma responsabilidade compreensível.

## Índice

- [Herança e composição](./01-heranca-e-composicao.md)
- [Properties, métodos de classe e dataclasses](./02-properties-e-dataclasses.md)

← [Erros](../11-Erros-e-Excecoes/README.md) | [Python intermediário →](../13-Python-Intermediario/README.md)
