# Sintaxe, indentação, comentários e nomes

## Sintaxe

Sintaxe são as regras que dizem como o código deve ser escrito. Python usa quebra de linha e **indentação** para agrupar blocos.

```python
idade = 20

if idade >= 18:
    print("Maior de idade")
```

As quatro espaços antes de `print` indicam que aquela linha pertence ao `if`. Não misture tabs e espaços; a convenção mais comum é quatro espaços por nível.

## Comentários

Use `#` para comentários que explicam uma decisão não óbvia:

```python
taxa_desconto = 0.10  # regra informada pela campanha atual
```

Não comente o que um nome claro já diz. `# soma um` acima de `contador += 1` geralmente não ajuda.

## Nomes

Use letras, números e `_`, sem começar por número. Prefira `snake_case` para variáveis e funções:

```python
preco_final = 49.90
quantidade_itens = 3
```

Evite nomes genéricos como `x`, `dados2` e `coisa` quando o significado importa. Também não use palavras reservadas como `if`, `for`, `class` ou `list` como nome.

## Atividade

Crie duas variáveis com nomes descritivos e mostre-as com `print`. Depois troque os valores e execute novamente.

← [Primeiro programa](./README.md) | [Fundamentos →](../03-Fundamentos/README.md)
