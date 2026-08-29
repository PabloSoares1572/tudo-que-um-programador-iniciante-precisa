# Instalação e reinstalação do Windows

> 🟢 **Nível:** iniciante, com atenção máxima à escolha de disco.  
> ⚠️ Não use mídia de terceiros, ISOs “modificadas” ou ativadores.

## Antes de iniciar

Complete o [checklist de formatação](../FORMATAR-PC.md#checklist-antes-de-formatar). Em especial, guarde chave de recuperação BitLocker, backup de documentos e drivers de rede quando o fabricante os disponibilizar.

## Mídia oficial

Use [download oficial do Windows](https://www.microsoft.com/software-download/windows11) e a [orientação de criação de mídia](https://support.microsoft.com/windows/deployment/install-upgrade/create-installation-media-for-windows). A ferramenta oficial é o ponto de partida mais seguro para criar pendrive de instalação.

## Fluxo seguro

1. Baixe mídia oficial.
2. Crie pendrive em dispositivo vazio.
3. Faça boot pelo **Boot Menu** na entrada UEFI do pendrive.
4. Selecione idioma e teclado.
5. Escolha instalação ou reparo conforme seu objetivo.
6. Ao escolher disco, confira capacidade, modelo e partições.
7. Para instalação limpa, apague somente partições do disco que você confirmou ser o alvo — e somente após backup.
8. Siga o primeiro boot sem desligar.
9. Atualize, instale drivers, ative legitimamente e restaure arquivos.

## UEFI, Secure Boot e TPM

Windows 11 exige um ambiente compatível com UEFI/Secure Boot e TPM 2.0 conforme requisitos oficiais. Entre no firmware apenas para checar/mudar configuração necessária. Fotografe ou anote o estado original. Mudar CSM/Legacy ou modo SATA sem plano pode impedir outro sistema de iniciar.

## Particionamento em linguagem simples

O instalador pode criar automaticamente partições de sistema, EFI e recuperação. Para usuário iniciante que fará instalação limpa em um único disco, o caminho mais seguro costuma ser deixar o instalador gerenciar o espaço do disco confirmado. Em dual boot ou vários discos, pare e use o [guia de dual boot](../DUAL-BOOT.md).

## Ativação legítima

- Use licença digital vinculada à sua conta/dispositivo ou chave válida.
- Se o PC veio com Windows, a ativação pode ocorrer automaticamente ao conectar à internet, dependendo da licença.
- Para problemas de ativação, use o solucionador oficial e suporte Microsoft/fabricante.
- Nunca execute ativadores, cracks, KMS não autorizado ou scripts de “licença grátis”. Além de ilegal, podem comprometer segurança.

## Como confirmar que terminou

- Windows inicia sem pendrive.
- Windows Update conclui atualizações.
- Rede, áudio, vídeo e armazenamento funcionam.
- Gerenciador de Dispositivos não mostra erro inesperado.
- Licença está ativada de forma legítima, se aplicável.
- Backup está configurado e arquivos foram restaurados com sucesso.
