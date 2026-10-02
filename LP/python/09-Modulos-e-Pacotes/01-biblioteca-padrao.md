# Biblioteca padrão: use o que já existe

A biblioteca padrão acompanha Python e resolve muitos problemas sem instalar pacotes extras.

| Módulo | Uso típico |
| --- | --- |
| `math` | operações matemáticas |
| `random` | sorteios e simulações não criptográficas |
| `datetime` | datas e horários |
| `pathlib` | caminhos e arquivos de forma multiplataforma |
| `json` / `csv` | formatos de dados comuns |
| `collections` | coleções especializadas |
| `itertools` | iteração eficiente |
| `statistics` | estatísticas básicas |
| `re` | expressões regulares |
| `logging` | registros de execução |

## Exemplo com `pathlib`

```python
from pathlib import Path

arquivo = Path("dados") / "notas.txt"
print(arquivo)
```

`Path` evita montar caminhos manualmente com barras diferentes entre sistemas.

## Atenção a segurança

`random` não é indicado para senhas, tokens ou chaves. Para isso, use `secrets`. `subprocess` e `os` também existem, mas só devem ser usados depois de entender validação, caminhos e risco de executar comandos externos.

← [Módulos](./README.md) | [`__main__` →](./02-main-e-organizacao.md)
