# Arquivos e JSON

\`\`\`python
from pathlib import Path
import json

caminho = Path("dados") / "arquivo.json"

with caminho.open("w", encoding="utf-8") as arquivo:
    json.dump({"ativo": True}, arquivo, ensure_ascii=False, indent=2)

with caminho.open("r", encoding="utf-8") as arquivo:
    dados = json.load(arquivo)
\`\`\`

- \`\"w\"\` sobrescreve; \`\"a\"\` adiciona; \`\"r\"\` lê.
- Use \`with\` e \`encoding=\"utf-8\"\`.
- Confirme caminho e trabalhe em dados de teste.

