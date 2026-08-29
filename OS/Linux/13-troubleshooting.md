# 13 — Troubleshooting Linux

## Método em seis passos

1. **Sintoma:** o que, quando e em qual contexto falha?
2. **Preservação:** há dados que precisam de backup antes de agir?
3. **Evidência:** mensagens, logs, versão, hardware, alterações recentes.
4. **Hipótese:** uma causa por vez, da mais simples à mais provável.
5. **Mudança mínima:** teste reversível e documentado.
6. **Confirmação:** reproduza cenário que falhava e registre solução/rollback.

## Sistema não inicia

**Possíveis causas:** disco não detectado, bootloader, kernel, initramfs, `fstab`, atualização ou hardware.  
**Diagnóstico:** fotografe mensagem, confira firmware/Boot Menu, inicie Live USB e monte somente para leitura quando possível.  
**Solução:** siga documentação da sua distribuição para recuperação de boot; não copie comando GRUB de outro sistema.  
**Confirmação:** dois boots completos sem USB.

## Sem Wi‑Fi/rede

**Diagnóstico:** `ip addr`, NetworkManager, interruptor físico, modo avião, logs e outro adaptador/rede.  
**Solução:** atualizar sistema/driver pela distribuição ou fabricante; não instalar pacote aleatório.  
**Confirmação:** IP, rota e DNS funcionam depois de reiniciar.

## Áudio, Bluetooth, GPU ou segundo monitor

**Diagnóstico:** cabo/porta, saída correta, configuração do ambiente gráfico, `lspci`/logs e driver oficial da distribuição.  
**Solução:** altere uma variável por vez; para GPU proprietária, use o método recomendado pela distro.  
**Desfazer:** mantenha kernel/driver anterior quando o gerenciador permitir e saiba entrar em modo de recuperação.

## Disco cheio

**Diagnóstico:** `df -h`, logs, cache de pacotes, snapshots e diretórios grandes.  
**Solução:** remova arquivos conhecidos, limpe cache pelo gerenciador e revise política de logs/snapshots.  
**Evite:** apagar `/var` ou arquivos de sistema às cegas.

## Atualização falhou

**Diagnóstico:** leia mensagem completa, espaço disponível, repositórios de terceiros, energia/rede e versão.  
**Solução:** recupere consistência conforme gerenciador de pacotes da família; não misture instruções de outra distro.  
**Confirmação:** atualizador conclui e o sistema reinicia sem erro.
