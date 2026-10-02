# 22 — Python no backend web

> ⚫ **Profissional**

Python pode atender requisições web, renderizar páginas, expor APIs, processar tarefas e conversar com banco de dados. O backend não é “só rotas”: envolve validação, autenticação, observabilidade, deploy e manutenção.

## Frameworks relevantes

| Ferramenta | Quando costuma fazer sentido |
| --- | --- |
| FastAPI | APIs com tipagem, validação e documentação |
| Django | aplicação web completa com ORM, admin e convenções |
| Flask | aplicação menor/flexível; você escolhe mais componentes |

Não comece aprendendo os três ao mesmo tempo. Escolha uma rota após dominar HTTP, Python, banco básico e testes.

## Arquitetura transferível

Independente do framework: separe entrada HTTP, validação, regra de negócio, persistência e integração externa. Proteja configurações, registre erros, teste rotas e mantenha migrações do banco versionadas.

## Próximo

- [Arquitetura de aplicação web](./01-arquitetura-web.md)
- [Projetos](../Projetos/README.md)

← [Automação](../21-Automacao/README.md) | [Concorrência →](../23-Concorrencia/README.md)

