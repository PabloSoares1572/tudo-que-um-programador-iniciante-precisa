# 21 — Automação responsável

> 🟡 **Intermediário**

Automação executa tarefas repetitivas com previsibilidade. Bons projetos começam pequenos e são reversíveis: organizar uma pasta de teste, gerar relatório CSV ou consultar uma API autorizada.

## Ideias seguras

- renomear arquivos dentro de diretório de teste;
- ler CSV e gerar resumo;
- gerar relatórios a partir de dados locais;
- baixar dados de uma API permitida com limites;
- organizar fotos/documentos apenas depois de simular a ação.

## Fluxo seguro

\`\`\`text
Listar alvo → validar regras → modo simulação → registrar ações → executar → confirmar resultado
\`\`\`

Use \`pathlib\`, \`csv\`, \`json\`, \`logging\` e testes. Para planilhas/PDFs, trate arquivos recebidos como dados não confiáveis e preserve cópias originais.

## Não faça

- automação de spam, scraping que viole regras, ataque, fraude ou invasão;
- exclusão/movimentação em massa sem modo de simulação e backup;
- executar comandos de shell compostos com entrada do usuário.

## Próximo

- [Projeto organizador seguro](../Projetos/07-organizador-de-arquivos.md)
- [Automação, shell e segurança](./01-shell-e-automacao-segura.md)

← [APIs](../20-APIs/README.md) | [Web →](../22-Web/README.md)

