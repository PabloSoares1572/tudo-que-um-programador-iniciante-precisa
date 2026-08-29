# Cheat sheet — Troubleshooting

1. Descreva sintoma e horário.
2. Anote alteração recente.
3. Preserve dados e não apague logs.
4. Colete: `systemctl status`, `journalctl -b -p err`, `ip addr`, `ip route`, `df -h`, `lsblk -f` conforme caso.
5. Teste uma hipótese por vez.
6. Faça mudança reversível.
7. Confirme com o mesmo cenário que falhava.
8. Documente causa, solução e rollback.

> ⚠️ “Reinstalar tudo” é último recurso. Primeiro salve dados e determine se problema é hardware, configuração, serviço, driver, rede ou atualização.
