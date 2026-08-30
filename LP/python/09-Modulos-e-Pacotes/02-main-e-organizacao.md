# `__name__`, `__main__` e organização

Um arquivo pode ser executado diretamente ou importado. A guarda abaixo permite deixar exemplos/testes manuais sem executá-los durante o import:

```python
def calcular_area(largura, altura):
    return largura * altura


if __name__ == "__main__":
    print(calcular_area(3, 4))
```

Quando o arquivo é executado diretamente, `__name__` vale `"__main__"`. Quando é importado, recebe o nome do módulo.

## Evite imports circulares

Se `a.py` importa `b.py` e `b.py` importa `a.py`, o projeto pode quebrar durante a inicialização. Em vez de “consertar” com import dentro de funções sem entender, reveja responsabilidades: talvez existe um terceiro módulo compartilhado ou uma dependência invertida.

## Convenção de pastas

Use nomes minúsculos e claros. Separe lógica de negócio, interfaces de entrada/saída e persistência conforme o projeto cresce. Não crie dez camadas para um script de 30 linhas; estrutura deve acompanhar a complexidade real.

← [Biblioteca padrão](./01-biblioteca-padrao.md) | [Arquivos →](../10-Arquivos/README.md)
