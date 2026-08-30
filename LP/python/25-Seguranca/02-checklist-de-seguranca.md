# Checklist de segurança antes de publicar

- [ ] Segredos não estão no código, commit, logs ou exemplos.
- [ ] \`.env\` e ambientes virtuais estão no \`.gitignore\`.
- [ ] Entradas externas têm validação e limites.
- [ ] Queries usam parâmetros.
- [ ] Operações em arquivos restringem-se à pasta permitida.
- [ ] Chamadas externas têm timeout e tratamento de falha.
- [ ] Dependências foram revisadas/atualizadas com fonte confiável.
- [ ] Erros públicos não exibem traceback ou configuração interna.
- [ ] Autenticação e autorização foram testadas separadamente.
- [ ] Backup/recuperação e permissões mínimas foram considerados.

Uma checklist não substitui revisão especializada, mas evita esquecer o básico repetidamente.

← [Configuração](./01-configuracao-e-validacao.md) | [Boas práticas →](../26-Boas-Praticas/README.md)

