# JSON e CSV

## JSON

JSON representa dados com objetos, listas, texto, números, booleanos e nulo. Em Python, objetos JSON viram normalmente dicionários e listas.

```python
import json
from pathlib import Path

dados = {"nome": "Ana", "ativo": True}
caminho = Path("usuario.json")

with caminho.open("w", encoding="utf-8") as arquivo:
    json.dump(dados, arquivo, ensure_ascii=False, indent=2)

with caminho.open("r", encoding="utf-8") as arquivo:
    usuario = json.load(arquivo)
```

Não confunda JSON com banco de dados. Ele serve bem para configuração ou dados pequenos e simples; múltiplas escritas concorrentes e consultas complexas pedem outra solução.

## CSV

CSV é comum em planilhas e tabelas simples. Use o módulo `csv`, pois delimitadores, aspas e quebras de linha têm regras próprias.

```python
import csv

with open("notas.csv", "w", newline="", encoding="utf-8") as arquivo:
    escritor = csv.DictWriter(arquivo, fieldnames=["nome", "nota"])
    escritor.writeheader()
    escritor.writerow({"nome": "Ana", "nota": 9})
```

Para ler, `csv.DictReader` devolve cada linha como dicionário. Valide campos e codificação de arquivos recebidos de terceiros.

← [Arquivos](./README.md) | [Escrita segura →](./02-caminhos-e-escrita-segura.md)
