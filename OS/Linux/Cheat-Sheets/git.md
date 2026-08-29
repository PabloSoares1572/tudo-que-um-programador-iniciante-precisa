# Cheat sheet — Git básico

| Objetivo | Comando | Cuidado |
| --- | --- | --- |
| Ver estado | `git status` | Sempre comece aqui |
| Ver mudanças | `git diff` | Revise antes de adicionar |
| Adicionar arquivo | `git add arquivo` | Evite `git add .` sem revisar |
| Criar commit | `git commit -m "mensagem"` | Mensagem explica intenção |
| Ver histórico | `git log --oneline` | Leitura |
| Criar branch | `git switch -c nome` | Isola mudança |
| Trocar branch | `git switch nome` | Verifique estado antes |

Não use `reset --hard`, `push --force` ou comandos destrutivos sem saber exatamente o impacto e ter backup/branch.
