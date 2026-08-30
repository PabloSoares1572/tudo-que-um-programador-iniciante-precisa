# \`pip\`, requirements e conflitos de dependência

## Operações básicas

\`\`\`text
python -m pip install nome-do-pacote
python -m pip uninstall nome-do-pacote
python -m pip install --upgrade nome-do-pacote
python -m pip show nome-do-pacote
\`\`\`

Leia a página oficial e verifique o nome correto no índice de pacotes antes de instalar. Pacotes com nomes parecidos podem ser maliciosos ou não relacionados.

## Reproduzir ambiente

Uma forma simples de registrar dependências é:

\`\`\`text
python -m pip freeze > requirements.txt
python -m pip install -r requirements.txt
\`\`\`

Em projetos profissionais, avalie estratégia de dependências/lockfile e \`pyproject.toml\`. \`requirements.txt\` é útil, mas não explica sozinho o propósito de cada pacote.

## Conflitos

Se uma biblioteca exige versões incompatíveis, não “force” sem avaliar. Leia as mensagens do resolvedor, verifique versões suportadas e atualize ou separe projetos. Nunca copie comandos de instalação com índices de pacote desconhecidos sem confirmar a origem.

← [Ambientes](./README.md) | [\`pyproject.toml\` e Git →](./02-pyproject-e-git.md)

