# CachyOS

## Visão geral

| Item | Descrição |
| --- | --- |
| Família/base | Arch Linux, com otimizações/pacotes próprios |
| Filosofia | Desktop de desempenho e kernels/configurações voltados a hardware atual, conforme projeto |
| Lançamento | Rolling release |
| Dificuldade | 🟡/🔴 |
| Pacotes | Pacman e repositórios próprios/Arch |

## Para que serve

CachyOS mira usuários que querem Arch-like com escolhas de performance e ferramenta/guias do projeto. “Otimizado” não garante mais FPS ou menor latência no seu PC; teste e meça.

## Pontos positivos

- opções de kernel/configuração voltadas a performance;
- instalador e experiência desktop;
- acesso ao ecossistema Arch para usuários que aceitam rolling release.

## Pontos de atenção

- kernels/repos próprios ampliam necessidade de acompanhar documentação;
- tuning pode adicionar variáveis no troubleshooting;
- não use em produção crítica sem testes/rollback.

## Para quem recomendo / não recomendo

**Recomendo** para usuário já confortável com Arch-like, jogos/desktop e teste de desempenho.  
**Não recomendo** para iniciante absoluto, servidor ou quem espera manutenção zero.

## Requisitos, desktop e pacotes

Consulte [CachyOS](https://cachyos.org/) para ISO, requisitos e notas da imagem atual. Pacotes seguem ecossistema Pacman com particularidades do projeto.

## Instalação específica

1. Baixe ISO oficial e teste live USB antes de remover Windows.
2. Registre kernel/configuração escolhidos durante instalador.
3. Em dual boot, preserve Windows/EFI e valide seus jogos antes de depender só do Linux.
4. Atualize como sistema rolling completo e consulte changelog do projeto.
5. Meça efeito de otimizações antes/depois; não aplique tweaks aleatórios.
