# Cheat sheet — Processos e systemd

| Objetivo | Comando | Efeito |
| --- | --- | --- |
| Ver processos | `ps aux` | Leitura |
| Monitorar | `top` / `htop` | Leitura dinâmica |
| Estado de serviço | `systemctl status servico` | Leitura |
| Iniciar/parar | `sudo systemctl start/stop servico` | Altera estado atual |
| Reiniciar | `sudo systemctl restart servico` | Pode interromper serviço |
| Habilitar boot | `sudo systemctl enable servico` | Altera inicialização futura |
| Logs de boot | `journalctl -b` | Leitura |
| Logs de serviço | `journalctl -u servico` | Leitura |

Sempre comece por `status` e logs antes de parar/reiniciar.
