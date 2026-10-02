# \`pyproject.toml\` e Git para projetos Python

## \`pyproject.toml\`

É um arquivo TOML usado por ferramentas de empacotamento e também por formatadores, linters, verificadores de tipo e testes. Em projetos distribuíveis, ele descreve metadados e sistema de build; em outros, pode centralizar configuração de ferramentas.

Exemplo mínimo ilustrativo:

\`\`\`toml
[project]
name = "minha-aplicacao"
version = "0.1.0"
requires-python = ">=3.12"
\`\`\`

Não copie versões de dependência sem entender compatibilidade. Consulte o guia de packaging quando for empacotar/publicar.

## Git: mínimo indispensável

\`\`\`text
git init
git status
git add .
git commit -m "cria base do projeto"
\`\`\`

Use commits pequenos que expliquem mudança. Crie branch para alteração isolada e revise antes de mesclar.

## \`.gitignore\`

Não versione \`.venv/\`, \`__pycache__/\`, \`.env\`, chaves, tokens, arquivos de cobertura e banco local de desenvolvimento, salvo decisão consciente. Exemplo:

\`\`\`text
.venv/
__pycache__/
.env
*.pyc
\`\`\`

Se um segredo entrou no Git, removê-lo do arquivo não basta: revogue/rotacione o segredo e siga procedimento de limpeza do histórico se necessário.

← [\`pip\`](./01-pip-requirements-e-conflitos.md) | [Banco de dados →](../19-Banco-de-Dados/README.md)

