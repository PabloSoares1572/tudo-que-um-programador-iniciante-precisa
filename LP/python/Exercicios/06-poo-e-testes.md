# Exercícios — POO e testes

## 🟡 1. Classe Produto

**Requisitos:** atributos nome, preço e estoque. Método \`baixar_estoque\` deve recusar valor não positivo e estoque insuficiente.

## 🔴 2. Dataclass de tarefa

**Requisitos:** use \`@dataclass\` para uma tarefa com título e concluída; crie método para concluir.

## 🔴 3. Testes pytest

**Requisitos:** escreva testes para caso normal, estoque exato e cada erro de \`baixar_estoque\`.

## ⚫ 4. Separação de responsabilidades

**Requisitos:** extraia regra de desconto de uma interface de terminal. Teste a regra sem chamar \`input()\` ou \`print()\`.

---

## Solução de referência — classe Produto

\`\`\`python
class Produto:
    def __init__(self, nome, preco, estoque):
        self.nome = nome
        self.preco = preco
        self.estoque = estoque

    def baixar_estoque(self, quantidade):
        if quantidade <= 0:
            raise ValueError("Quantidade deve ser positiva")
        if quantidade > self.estoque:
            raise ValueError("Estoque insuficiente")
        self.estoque -= quantidade
\`\`\`

## Solução de referência — testes

\`\`\`python
import pytest

def test_baixar_estoque():
    produto = Produto("Teclado", 100, 2)
    produto.baixar_estoque(2)
    assert produto.estoque == 0

def test_nao_aceita_estoque_insuficiente():
    produto = Produto("Teclado", 100, 1)
    with pytest.raises(ValueError, match="insuficiente"):
        produto.baixar_estoque(2)
\`\`\`

← [Arquivos e exceções](./05-arquivos-e-excecoes.md) | [Aplicações →](./07-aplicacoes.md)

