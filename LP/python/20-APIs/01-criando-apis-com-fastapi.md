# Criando APIs: rotas, validação e respostas

FastAPI é uma opção moderna para criar APIs Python com tipagem e documentação automática. A ferramenta não substitui regras de negócio, autenticação, testes ou segurança.

Exemplo mínimo conceitual:

\`\`\`python
from fastapi import FastAPI

app = FastAPI()

@app.get("/saude")
def verificar_saude() -> dict[str, str]:
    return {"status": "ok"}
\`\`\`

Para executar, siga a documentação da versão usada e mantenha dependências no ambiente virtual. Em produção, não exponha modo de desenvolvimento e não trate a rota de saúde como autenticação.

## Projeto de API

Organize rotas, schemas/validação, serviços, persistência e configuração. Comece simples; extraia camadas quando houver responsabilidade real, não porque um diagrama de arquitetura mandou.

← [APIs](./README.md) | [Contratos e segurança →](./02-contratos-e-seguranca.md)

