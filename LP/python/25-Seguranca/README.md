# 25 — Segurança em Python

> ⚫ **Profissional**

Segurança não é um módulo que você “ativa” no final. Ela é parte de entrada, dependências, configuração, logs, banco, APIs e deploy.

## Base de segurança

1. Valide toda entrada externa.
2. Use consultas parametrizadas no banco.
3. Guarde segredos em variáveis de ambiente/serviço de segredos, nunca no Git.
4. Use dependências confiáveis, atualizadas e com versões revisadas.
5. Aplique menor privilégio para banco, arquivos e APIs.
6. Registre eventos úteis sem registrar senha/token/dados sensíveis.
7. Trate erros sem vazar detalhes internos ao usuário.
8. Faça backup e teste recuperação quando houver dados relevantes.

## Ameaças abordadas

- SQL injection;
- command injection;
- path traversal;
- exposição de segredos;
- autenticação/autorização incompleta;
- dependência comprometida;
- desserialização não confiável;
- logs com dados sensíveis.

## Índice

- [Configuração, segredos e validação](./01-configuracao-e-validacao.md)
- [Checklist de revisão](./02-checklist-de-seguranca.md)

← [Performance](../24-Performance/README.md) | [Boas práticas →](../26-Boas-Praticas/README.md)

