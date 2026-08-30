# 20 — APIs e HTTP

> 🟡 **Intermediário**

Uma API é uma interface para programas conversarem. Na web, é comum usar HTTP, URLs e JSON.

| Termo | Significado |
| --- | --- |
| cliente | programa que faz a requisição |
| servidor | programa que recebe e responde |
| endpoint | endereço/rota da API |
| request | pedido HTTP |
| response | resposta HTTP |
| header | metadado da requisição/resposta |
| status code | resultado, como 200, 404 ou 500 |

## Consumindo API de forma segura

Com uma biblioteca HTTP instalada no ambiente virtual, defina timeout, verifique status e valide o formato recebido.

\`\`\`python
import requests

resposta = requests.get("https://api.exemplo.test/usuarios", timeout=10)
resposta.raise_for_status()
dados = resposta.json()
\`\`\`

O endereço acima é ilustrativo. Em um projeto real, consulte documentação do serviço, respeite limites/termos e nunca deixe tokens no código.

## Índice

- [Criando APIs com FastAPI](./01-criando-apis-com-fastapi.md)
- [Autenticação, erros e documentação](./02-contratos-e-seguranca.md)

← [Banco de dados](../19-Banco-de-Dados/README.md) | [Automação →](../21-Automacao/README.md)

