# 03 — Curso progressivo de terminal

O terminal é uma maneira de conversar com o sistema por texto. Ele não é “modo hacker”; é uma ferramenta precisa para navegar, automatizar, diagnosticar e administrar.

## Ordem de estudo

1. [Primeiros comandos](./01-primeiros-comandos.md)
2. [Arquivos e diretórios](./02-arquivos-e-diretorios.md)
3. [Pipes e redirecionamento](./03-pipes-e-redirecionamento.md)
4. [Busca e filtros](./04-busca-e-filtros.md)
5. [Comandos avançados e segurança](./05-comandos-avancados-e-seguros.md)

## Regras do terminal

- A linha não pede confirmação “por educação”; ela faz o que foi digitado.
- Espaços, maiúsculas/minúsculas e caminho correto importam.
- Leia `man comando` ou `comando --help` antes de usar opções desconhecidas.
- Comece em `~/linux-pratica`, não em `/`.
- Use `-i` em `cp`, `mv` e `rm` quando estiver aprendendo, pois pede confirmação em casos de sobrescrita/remoção.

> ⚠️ Nunca cole um bloco inteiro de comandos que você não entende, principalmente se contiver `sudo`, `rm`, `dd`, `mkfs`, `chmod -R`, redirecionamento com `>` ou nome de disco como `/dev/sdX`.
