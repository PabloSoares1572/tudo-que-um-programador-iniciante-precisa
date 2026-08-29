# Cheat sheet — Rede

| Objetivo | Comando | Observação |
| --- | --- | --- |
| Interfaces/IP | `ip addr` | Dados locais; não publique sem necessidade |
| Rotas/gateway | `ip route` | Mostra rota padrão |
| Testar conectividade | `ping -c 4 host` | Ping bloqueado não prova falha sozinho |
| Portas abertas | `ss -tulpn` | Pode precisar sudo para detalhes |
| Testar HTTP | `curl -I URL` | Cabeçalhos, sem baixar página toda |
| Testar download | `wget --spider URL` | Não baixa conteúdo |
| Wi‑Fi/NetworkManager | `nmcli` | Consulte `nmcli --help` antes de alterar |

Em servidor remoto, não mude rota/DNS/firewall sem console ou plano de recuperação.
