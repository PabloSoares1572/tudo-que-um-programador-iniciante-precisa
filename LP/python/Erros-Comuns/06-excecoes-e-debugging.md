# Exceções escondidas e debugging sem adivinhação

## Erro

Usar \`except:\` ou \`except Exception:\` para retornar valor genérico e fazer o bug desaparecer.

## Por que acontece

A intenção é “não quebrar”, mas a causa fica invisível e o programa pode continuar com dados incorretos.

## Exemplo incorreto

\`\`\`python
try:
    return int(texto)
except:
    return 0
\`\`\`

Texto inválido vira idade zero silenciosamente.

## Como corrigir

Capture exceção específica, comunique regra e registre contexto quando necessário:

\`\`\`python
try:
    return int(texto)
except ValueError as erro:
    raise ValueError("Informe número inteiro") from erro
\`\`\`

## Como evitar

Leia traceback, reproduza caso mínimo e escreva teste de regressão. Um erro claro é melhor que resultado falso.

