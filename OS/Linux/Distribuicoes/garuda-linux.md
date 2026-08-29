# Garuda Linux

## Visão geral

| Item | Descrição |
| --- | --- |
| Família/base | Arch Linux |
| Filosofia | Desktop Arch-like com ferramentas, visual e snapshots conforme edição |
| Lançamento | Rolling release |
| Dificuldade | 🟡/🔴 |
| Pacotes | Pacman e ecossistema Arch/projeto |

## Para que serve

Garuda Linux pode agradar a usuário que quer desktop visualmente pronto, recursos de snapshot e ecossistema Arch. A aparência não substitui entendimento de atualização, Btrfs/snapshots e pacotes.

## Pontos positivos

- experiência desktop com várias escolhas de interface;
- ferramentas/snapshots em cenários suportados;
- acesso a pacote e documentação do ecossistema Arch.

## Pontos de atenção

- maior personalização pode significar mais componentes para entender;
- snapshots consomem disco e não substituem backup externo;
- rolling release pede manutenção responsável.

## Para quem recomendo / não recomendo

**Recomendo** para usuário intermediário que gosta de Arch-like e quer recuperação por snapshots.  
**Não recomendo** para primeiro Linux sem VM/backup, servidor ou PC com armazenamento muito apertado.

## Requisitos, desktop e pacotes

Consulte [Garuda Linux](https://garudalinux.org/) para edições, requisitos e guia de instalação. Use Pacman/ferramentas do projeto conforme documentação atual.

## Instalação específica

1. Escolha edição/desktop pelo hardware e objetivo, não apenas pelo tema.
2. Teste live USB e confirme capacidade de disco, principalmente se snapshots estiverem envolvidos.
3. Em dual boot, use espaço não alocado e faça backup completo antes de configurar Btrfs manualmente.
4. Atualize sistema inteiro; leia avisos antes de mudanças grandes de kernel/boot.
5. Teste restauração de snapshot em ambiente seguro antes de confiar nela.
