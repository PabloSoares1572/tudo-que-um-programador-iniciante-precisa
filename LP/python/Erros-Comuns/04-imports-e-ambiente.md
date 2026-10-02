# Imports, pacote instalado no Python errado e ambiente virtual

## Erro

\`ModuleNotFoundError\` mesmo depois de instalar pacote.

## Por que acontece

O pacote pode ter sido instalado em outro interpretador/ambiente, ou seu arquivo local possui mesmo nome do módulo, como \`json.py\` ou \`requests.py\`.

## Como diagnosticar

\`\`\`text
python --version
python -m pip --version
python -c "import sys; print(sys.executable)"
\`\`\`

Os caminhos precisam apontar para o mesmo ambiente.

## Como corrigir

Ative o ambiente virtual do projeto e instale com \`python -m pip install pacote\`. Renomeie arquivo local que colide com biblioteca e apague \`__pycache__\` somente se necessário, dentro do projeto correto.

## Como evitar

Use uma \`.venv\` por projeto, abra a pasta do projeto no editor e versiona apenas arquivos de configuração/dependências, não a pasta virtual.

