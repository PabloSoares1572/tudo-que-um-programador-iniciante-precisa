# Caminhos e escrita segura

## Use `pathlib`

```python
from pathlib import Path

base = Path("dados_teste")
base.mkdir(exist_ok=True)
arquivo = base / "resultado.txt"
```

Isso torna a intenção mais clara e funciona melhor em sistemas diferentes que juntar strings com `/` ou `\\` manualmente.

## Antes de sobrescrever

1. trabalhe numa pasta de teste;
2. mostre/registre o caminho alvo;
3. faça backup se os dados forem importantes;
4. prefira gravar em arquivo temporário e renomear quando a operação for crítica;
5. trate falhas de permissão e disco cheio.

## Não confie em caminhos recebidos

Em aplicações web ou automações, um nome de arquivo vindo do usuário pode tentar sair da pasta esperada com `../`. Nunca concatene esse valor diretamente em um caminho de servidor. Valide/normalize, limite a uma pasta permitida e mantenha a operação sob controle — tema retomado em [segurança](../25-Seguranca/README.md).

← [JSON e CSV](./01-json-e-csv.md) | [Erros e exceções →](../11-Erros-e-Excecoes/README.md)
