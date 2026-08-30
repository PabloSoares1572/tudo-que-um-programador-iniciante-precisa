# Tuplas e unpacking

Tuplas são sequências imutáveis. Use-as quando a posição tem significado e a coleção não deve ser alterada acidentalmente.

```python
coordenada = (10, 20)
x, y = coordenada
```

O segundo exemplo é **unpacking**: os elementos são atribuídos a variáveis na mesma ordem.

## Quando usar

- retorno de vários valores de uma função;
- coordenadas, configurações fixas e pares de dados;
- chave de dicionário quando todos os valores internos forem imutáveis.

Não escolha tupla só porque “é mais rápida”. Escolha porque a imutabilidade comunica uma regra útil.

## Erro comum

Uma tupla com um elemento precisa de vírgula:

```python
um_item = ("Python",)
```

Sem vírgula, é apenas uma string entre parênteses.

← [Listas](./01-listas.md) | [Dicionários →](./03-dicionarios.md)
