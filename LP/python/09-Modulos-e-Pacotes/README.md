# 09 — Módulos e pacotes

> 🟡 **Intermediário inicial**

Um módulo é, em geral, um arquivo `.py` que pode ser importado. Um pacote organiza módulos em uma pasta. Essa divisão evita que um único arquivo acumule todas as responsabilidades.

```python
import math

raiz = math.sqrt(81)
```

## Formas de importar

```python
import datetime
from pathlib import Path
import json as json_mod
```

Evite `from modulo import *`: ele esconde de onde vêm os nomes e facilita conflitos.

## Organização simples

```text
meu_projeto/
├── main.py
└── calculos.py
```

Em `calculos.py`, defina funções; em `main.py`, importe e execute a aplicação. Não faça ações perigosas ou lentas automaticamente quando um módulo é importado.

## Índice

- [Biblioteca padrão](./01-biblioteca-padrao.md)
- [`__name__` e ponto de entrada](./02-main-e-organizacao.md)

← [Funções](../08-Funcoes/README.md) | [Arquivos →](../10-Arquivos/README.md)
