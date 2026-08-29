# Arch Linux

## Visão geral

| Item | Descrição |
| --- | --- |
| Família/base | Arch, independente |
| Filosofia | Simplicidade de projeto, controle do usuário e documentação detalhada |
| Lançamento | Rolling release |
| Dificuldade | 🔴 para instalação/administração inicial |
| Pacotes | Pacman; ecossistema de pacotes comunitários exige atenção extra |

## Para que serve

Arch é excelente para aprender como componentes Linux se encaixam e para quem quer controle sobre o sistema. A instalação e manutenção pedem leitura da documentação; isso é parte da proposta, não defeito a “pular” com script desconhecido.

## Pontos positivos

- ArchWiki é referência de documentação técnica;
- pacotes atuais e modelo rolling;
- alta flexibilidade de ambiente e componentes;
- aprendizado profundo de boot, rede, pacotes e desktop.

## Pontos de atenção

- instalação não é o caminho mais fácil para primeiro Linux;
- rolling release exige atualização completa e leitura de avisos;
- pacotes comunitários não devem ser tratados como repositório oficial sem revisão.

## Para quem recomendo / não recomendo

**Recomendo** para quem já entende terminal, backup e manutenção ou vai praticar em VM.  
**Não recomendo** como sistema principal de primeiro contato, servidor crítico sem experiência ou quem quer nunca ler documentação.

## Requisitos, desktop e pacotes

Baixe em [Arch Linux](https://archlinux.org/download/) e siga o [Installation guide](https://wiki.archlinux.org/title/Installation_guide). A ISO oficial é voltada a instalação por terminal; `archinstall` pode ajudar, mas não elimina a necessidade de entender escolhas.

## Instalação específica

1. Comece em VM e leia o guia inteiro antes de particionar.
2. Verifique checksum/assinatura conforme [Arch download](https://archlinux.org/download/).
3. Confirme UEFI, rede, hora, disco e partições com comandos de diagnóstico antes de escrever.
4. Não use `dd`, `mkfs`, `fdisk` ou script de instalação sem identificar o disco pelo modelo/tamanho.
5. Após instalar, configure bootloader, usuário, rede, atualização e desktop seguindo a Wiki.
6. Atualize o sistema inteiro com o método oficial; não faça atualização parcial.
