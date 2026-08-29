# Cheat sheet — Terminal

| Objetivo | Comando | Observação |
| --- | --- | --- |
| Ver pasta atual | `pwd` | Diagnóstico, sem alteração |
| Listar | `ls -la` | Inclui ocultos e detalhes |
| Entrar em pasta | `cd caminho` | `cd ..` sobe; `cd ~` vai para home |
| Criar pasta | `mkdir nome` | `mkdir -p a/b` cria intermediárias |
| Criar arquivo vazio | `touch arquivo` | Não adiciona conteúdo |
| Ler arquivo curto | `cat arquivo` | Prefira `less` em arquivo grande |
| Navegar leitura | `less arquivo` | `q` sai |
| Ver começo/fim | `head`, `tail` | `tail -f` acompanha log; `Ctrl+C` encerra |
| Ajuda | `man comando` | Leia antes de opção desconhecida |

> ⚠️ Antes de `rm`, `sudo`, `>` ou comandos em `/dev`: rode `pwd`/`ls`/`lsblk -f` e confirme o alvo.
