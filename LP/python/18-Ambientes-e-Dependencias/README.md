# 18 — Ambientes, \`pip\`, dependências e Git

> ⚫ **Profissional**

Cada projeto deve controlar seu interpretador e suas bibliotecas. Um ambiente virtual evita que o pacote de um projeto quebre outro ou o Python do sistema.

\`\`\`text
projeto-a → .venv com dependências A
projeto-b → .venv com dependências B
\`\`\`

## Criar ambiente virtual

\`\`\`text
Windows: py -m venv .venv
Linux/macOS: python3 -m venv .venv
\`\`\`

Ativação comum:

\`\`\`text
Windows PowerShell: .\.venv\Scripts\Activate.ps1
Windows cmd: .venv\Scripts\activate.bat
Linux/macOS: source .venv/bin/activate
\`\`\`

Depois, confirme qual Python está ativo e use \`python -m pip\`, não um \`pip\` solto que pode apontar para outro ambiente.

\`\`\`text
python --version
python -m pip install pytest
python -m pip list
\`\`\`

## Índice

- [\`pip\`, requirements e conflitos](./01-pip-requirements-e-conflitos.md)
- [\`pyproject.toml\` e Git](./02-pyproject-e-git.md)

> No Linux, não tente “resolver” instalação bloqueada usando \`sudo pip\`. Crie o ambiente virtual dentro do projeto. Isso evita interferir no Python administrado pela distribuição.

← [Debugging](../17-Debugging/README.md) | [Banco de dados →](../19-Banco-de-Dados/README.md)

