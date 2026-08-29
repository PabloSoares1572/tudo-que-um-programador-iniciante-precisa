# Instalação geral de distribuições Linux

Este guia evita repetir passos perigosos em todas as páginas. Cada distribuição tem instalador, imagem e particularidades próprias; leia também a página específica e a documentação oficial atual.

## 1. Defina o cenário

- instalação limpa em um disco dedicado;
- dual boot Windows + Linux;
- Linux em segundo SSD;
- máquina virtual;
- live USB apenas para teste.

Para dual boot, leia [Dual boot](../../DUAL-BOOT.md) antes. Não descubra particionamento no meio do instalador.

## 2. Baixe da fonte oficial

1. Abra o link oficial da distribuição escolhida.
2. Escolha arquitetura/edição/desktop compatível com seu PC.
3. Baixe ISO e, se disponível, checksum/assinatura.
4. Verifique integridade/autenticidade conforme instrução do projeto.

Debian, Fedora, Arch e Qubes, por exemplo, publicam documentação de verificação. A forma correta varia; não copie chave/comando de outro projeto.

## 3. Crie o pendrive

Use ferramenta conhecida, como Rufus, Ventoy ou a ferramenta oficial recomendada pelo projeto. Confira **modelo e tamanho do pendrive** antes de gravar — a operação apaga o dispositivo selecionado.

## 4. Inicie em modo live/instalador

Abra Boot Menu e selecione a entrada UEFI do pendrive. Quando houver modo live, teste pelo menos Wi‑Fi, teclado, áudio, vídeo, touchpad, rede e discos antes de instalar.

## 5. Particionamento

| Cenário | Direção segura |
| --- | --- |
| Disco dedicado vazio | Deixe instalador gerenciar o disco confirmado, se você é iniciante |
| Um disco com Windows | Use somente espaço não alocado e siga [dual boot](../../DUAL-BOOT.md) |
| Dois discos | Confirme modelo/capacidade e selecione apenas o SSD de destino |
| Criptografia/LVM/Btrfs manual | Faça em VM/laboratório ou com backup e guia específico |

> ⚠️ Não formate EFI, Windows, Recovery ou partições de dados porque “parecem pequenas” ou “não têm letra”. Leia o resumo final do instalador antes de confirmar.

## 6. Crie usuário e senha

Use senha forte e anote em gerenciador de senhas. Não use conta root para uso diário se a distribuição cria usuário normal com `sudo`.

## 7. Primeiro boot

1. Remova pendrive quando o instalador solicitar.
2. Confirme que o sistema inicia sem pendrive.
3. Rode atualização pelo método da distribuição.
4. Instale driver de GPU/hardware pelo canal recomendado.
5. Configure backup, idioma, fuso, navegador e programas.
6. Teste reiniciar, suspender e desligar.

## 8. Problemas comuns

| Sintoma | Diagnóstico inicial | Ação segura |
| --- | --- | --- |
| Pendrive não aparece | ISO/mídia/porta/UEFI | Recrie com fonte oficial e teste outra porta |
| Wi‑Fi não funciona | Driver/firmware/hardware | Teste live USB, cabo e documentação da distro |
| Disco não aparece | RST/RAID/cabo/driver | Não mude AHCI/RAID sem procedimento do fabricante |
| Linux não aparece após instalar | Entrada UEFI/bootloader | Use Boot Menu e guia oficial de recuperação |
| Tela preta/GPU | Driver/modo gráfico | Teste opção recomendada pela distribuição, sem instalar driver aleatório |

## 9. Checklist final

- [ ] Sistema inicia sem pendrive.
- [ ] Atualizações concluídas.
- [ ] Wi‑Fi, áudio, vídeo, Bluetooth e armazenamento testados.
- [ ] Backup configurado.
- [ ] Usuário normal funciona e `sudo` é usado conscientemente.
- [ ] Caso seja dual boot, Windows também inicia.
