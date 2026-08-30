# Contratos, autenticação e erros de API

## Contrato

Documente o que cada endpoint recebe e devolve: campos, tipos, status codes e erros. Mudanças incompatíveis precisam de versão ou plano de migração.

## Validação

Valide dados no limite da aplicação. Type hints ajudam ferramentas, mas um JSON externo pode estar incompleto, malformado ou malicioso. Responda com erro claro sem vazar stack trace interno.

## Autenticação x autorização

- **autenticação:** quem é a pessoa/serviço?
- **autorização:** essa identidade pode executar esta ação?

Não implemente login próprio copiando snippets ao acaso. Use hashes de senha adequados, segredo em variáveis de ambiente, HTTPS, expiração/rotação de tokens e biblioteca/documentação confiáveis.

## HTTP e erros

Use status coerentes: 2xx para sucesso, 4xx para problema do cliente/permissão e 5xx para falha do servidor. Registre detalhes internamente, mas não exponha credenciais, SQL ou traceback ao consumidor.

← [Criar APIs](./01-criando-apis-com-fastapi.md) | [Automação →](../21-Automacao/README.md)

