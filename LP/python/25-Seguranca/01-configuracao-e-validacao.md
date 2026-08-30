# Configuração, segredos e validação

## Variáveis de ambiente

Use ambiente para valores que mudam por instalação ou são sensíveis, como URL de banco e token. Valide presença e formato ao iniciar a aplicação.

\`\`\`python
import os

token = os.environ.get("MINHA_API_TOKEN")
if not token:
    raise RuntimeError("MINHA_API_TOKEN não foi configurada")
\`\`\`

O exemplo mostra como exigir configuração; não imprima o token em erro/log.

## Senhas

Nunca guarde senha em texto puro. Use biblioteca confiável para hash com algoritmo apropriado e parâmetros atuais; não crie criptografia própria.

## Desserialização

JSON é apropriado para dados simples. Não use \`pickle\` para dados de origem não confiável: ele pode executar código durante desserialização.

## Validação em camadas

Valide formato, tipo, limite e autorização. Sanitização não substitui validação; encoding de saída também é importante em web. Regras dependem do contexto da aplicação.

← [Segurança](./README.md) | [Checklist →](./02-checklist-de-seguranca.md)

