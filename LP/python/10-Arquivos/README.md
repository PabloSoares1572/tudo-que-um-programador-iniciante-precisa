# 10 — Arquivos, caminhos, JSON e CSV

> 🟡 **Intermediário inicial**

Arquivos persistem dados depois que o programa termina. Antes de escrever, saiba qual arquivo será alterado e use dados de teste quando estiver aprendendo.

## Ler e escrever com `with`

```python
from pathlib import Path

caminho = Path("anotacoes.txt")

with caminho.open("w", encoding="utf-8") as arquivo:
    arquivo.write("Primeira anotação\n")

with caminho.open("r", encoding="utf-8") as arquivo:
    conteudo = arquivo.read()

print(conteudo)
```

`with` fecha o arquivo mesmo se ocorrer um erro. O modo `"w"` sobrescreve o conteúdo existente; `"a"` adiciona ao final. Confirme o caminho antes de usar qualquer modo de escrita.

## Conteúdos relacionados

- [JSON e CSV](./01-json-e-csv.md)
- [Caminhos e escrita segura](./02-caminhos-e-escrita-segura.md)

← [Módulos](../09-Modulos-e-Pacotes/README.md) | [Erros e exceções →](../11-Erros-e-Excecoes/README.md)
