# 11 — Administração e armazenamento

## Administração é método

Um administrador profissional não começa pelo comando: começa por objetivo, inventário, risco, backup, mudança pequena, validação e registro.

## Tópicos essenciais

| Tema | O que aprender |
| --- | --- |
| Boot | UEFI, GRUB, kernel, initramfs e logs de inicialização |
| Montagem | `findmnt`, UUID, `/etc/fstab`, permissões e reversão |
| LVM | Volumes físicos, grupos e volumes lógicos; útil para flexibilidade |
| RAID | Redundância/desempenho conforme nível; não substitui backup |
| Filesystems | ext4, XFS, Btrfs e critérios de escolha |
| Backup | Política, retenção, criptografia e teste de restauração |
| Logs | journal, logs de serviço e rotação |

## `/etc/fstab` 🟡

`fstab` define montagens persistentes. Prefira UUID e teste a configuração em ambiente seguro. Erro pode parar boot/interromper montagem. Antes de reiniciar, valide sintaxe conforme documentação de sua distribuição e mantenha Live USB/console disponível.

## LVM e RAID 🔴

LVM facilita redimensionar e organizar volumes, mas aumenta camadas. RAID pode melhorar disponibilidade, mas não protege de exclusão, ransomware, erro humano ou desastre. Backup independente continua obrigatório.

## Backups que funcionam

1. Defina o que precisa recuperar: arquivo, banco, VM, sistema ou serviço completo.
2. Faça cópia automática conforme criticidade.
3. Proteja com criptografia quando houver dados sensíveis.
4. Guarde cópia fora do equipamento, quando necessário.
5. Faça restauração de teste periodicamente.

## Exercício 🔴

Escreva um plano de backup para uma VM de teste: dados, frequência, destino, retenção, teste de restauração e responsável. Não pratique criação de RAID/LVM em disco que tenha dados sem laboratório e backup.
