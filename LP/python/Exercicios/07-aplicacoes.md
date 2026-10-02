# Exercícios — aplicações

## 🟡 1. Requisição HTTP simulada

**Objetivo:** praticar contrato de API sem depender de servidor real.

**Requisitos:** crie uma função que recebe um dicionário de resposta e devolve nome de usuário válido ou levanta \`ValueError\`.

## 🔴 2. Consulta SQLite

**Requisitos:** crie tabela de tarefas, insira três itens e liste apenas pendentes usando query parametrizada.

## 🔴 3. Organizador em modo simulação

**Requisitos:** receba caminhos em pasta de teste, mostre os renomes planejados e só execute quando parâmetro \`confirmar=True\`.

## ⚫ 4. Limite de concorrência

**Requisitos:** modele várias tarefas assíncronas com \`asyncio\` e sem rede real; limite quantas podem rodar juntas. Explique por que não usar concorrência se a versão sequencial for suficiente.

---

## Solução de referência — validação de payload

\`\`\`python
def extrair_nome_usuario(payload):
    nome = payload.get("nome")
    if not isinstance(nome, str) or not nome.strip():
        raise ValueError("Payload sem nome válido")
    return nome.strip()
\`\`\`

## Critérios de qualidade

- timeout e tratamento de status existem em API real;
- SQL usa parâmetros;
- automação não aponta para pasta pessoal sem confirmação;
- tarefas assíncronas têm exceções observadas.

← [POO e testes](./06-poo-e-testes.md) | [Desafios →](../Desafios/README.md)

