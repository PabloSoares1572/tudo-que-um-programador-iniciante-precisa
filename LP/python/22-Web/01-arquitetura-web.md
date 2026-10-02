# Arquitetura web sem excesso de camadas

Um fluxo comum:

\`\`\`text
requisição HTTP → rota/controlador → validação → serviço/regra de negócio
→ repositório/persistência → resposta HTTP
\`\`\`

Nem todo projeto precisa de cada nome/camada. O objetivo é impedir que uma rota tenha 300 linhas misturando autorização, cálculo, SQL e formatação de resposta.

## Configuração

Use variáveis de ambiente para URLs, chaves e modo de execução. Não salve \`.env\` com segredos no Git. Separe desenvolvimento, teste e produção de forma explícita.

## Deploy

Antes de publicar: teste, defina logs, trate erros, configure HTTPS, migrações, backup e permissões mínimas. “Funciona no meu PC” não é plano de operação.

← [Web](./README.md) | [Concorrência →](../23-Concorrencia/README.md)

