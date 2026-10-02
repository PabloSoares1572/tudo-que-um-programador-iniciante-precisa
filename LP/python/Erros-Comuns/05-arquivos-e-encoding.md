# Caminhos, arquivos e encoding

## Erro

\`FileNotFoundError\`, \`PermissionError\` ou texto com caracteres estranhos.

## Por que acontece

O programa é executado em outra pasta, o caminho relativo não existe, falta permissão ou o arquivo tem codificação diferente.

## Exemplo mais seguro

\`\`\`python
from pathlib import Path

caminho = Path("dados_teste") / "texto.txt"
if not caminho.exists():
    raise FileNotFoundError(f"Arquivo não encontrado: {caminho}")
conteudo = caminho.read_text(encoding="utf-8")
\`\`\`

## Como corrigir

Mostre o caminho usado, confirme diretório atual e informe \`encoding="utf-8"\` quando controlar o arquivo. Para arquivo externo, descubra/registre a codificação correta em vez de trocar aleatoriamente.

## Como evitar

Use \`pathlib\`, diretórios de teste, backups e modos de escrita conscientes. \`\"w\"\` sobrescreve arquivo.

