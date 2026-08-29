# 07 — Discos e partições

> 🔴 Discos e partições exigem atenção. Primeiro identifique; só depois pense em alterar.

## Termos

| Termo | Explicação |
| --- | --- |
| HDD | Disco mecânico, geralmente maior/mais lento |
| SSD SATA | Armazenamento sólido conectado por SATA |
| NVMe | SSD que usa interface PCIe; costuma aparecer como `nvme0n1` |
| Partição | Parte lógica de um disco |
| Sistema de arquivos | Como dados são organizados: ext4, NTFS, FAT32 etc. |
| Ponto de montagem | Diretório onde uma partição fica acessível |
| Swap | Espaço de apoio à memória |
| LVM | Gerenciamento lógico de volumes, útil em administração |

## Diagnóstico seguro

~~~bash
lsblk -f
findmnt
df -h
sudo blkid
~~~

- `lsblk -f` mostra discos, partições e sistemas de arquivos.
- `findmnt` mostra montagens ativas.
- `df -h` mostra uso em sistemas montados.
- `blkid` mostra identificadores; use com cuidado e apenas leitura aqui.

Antes de qualquer ação, confirme modelo e tamanho físico. Nomes como `/dev/sda` podem mudar conforme dispositivos conectados; UUID é mais estável para montagens persistentes.

## Montagem manual

Uma unidade pode ser montada em diretório vazio, por exemplo em `/mnt` ou `/media`. A interface gráfica geralmente faz isso automaticamente para pendrives. Para servidor, siga documentação da distribuição e use UUID em `/etc/fstab` quando a montagem deve persistir.

> ⚠️ Uma linha errada em `/etc/fstab` pode dificultar ou impedir boot. Sempre valide sintaxe e mantenha acesso de recuperação antes de reiniciar.

## Sistemas de arquivos

| Sistema | Uso comum | Observação |
| --- | --- | --- |
| ext4 | Linux geral | Padrão frequente e maduro |
| Btrfs | Sistemas com snapshots/recursos avançados | Exige entender subvolumes e política de snapshots |
| XFS | Servidores/arquivos grandes | Tem particularidades de crescimento/reparo |
| NTFS | Windows e compartilhamento | Evite escrita pelo Linux se Windows estiver hibernado/Fast Startup |
| FAT32/exFAT | Mídias removíveis/compatibilidade | Não possuem os mesmos recursos de permissões Linux |

## Ferramentas perigosas

`fdisk`, `parted`, `mkfs`, `dd` e comandos de reparo podem apagar dados. Não há um comando universal seguro para “formatar /dev/sdX”. Para mudança real:

1. backup validado;
2. identificação por modelo/capacidade;
3. live USB/ambiente de manutenção se necessário;
4. plano de reversão;
5. guia específico da distribuição e cenário.

## Exercício 🟡

Rode `lsblk -f` e desenhe em papel a relação entre disco, partição, sistema de arquivos e ponto de montagem. Não altere nada.
