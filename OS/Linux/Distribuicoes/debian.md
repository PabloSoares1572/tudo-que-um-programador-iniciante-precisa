# Debian

## Visão geral

| Item | Descrição |
| --- | --- |
| Família/base | Debian, independente e base de muitas outras distribuições |
| Filosofia | Estabilidade, software livre e comunidade ampla |
| Lançamento | Versões estáveis com ciclo mais conservador; também há ramos de teste/instável para usos específicos |
| Dificuldade | 🟡 Intermediário amigável para quem lê documentação |
| Pacotes | APT e pacotes `.deb` |

## Para que serve

Debian é forte para servidores, desenvolvimento, desktop estável e quem quer entender uma base importante do ecossistema Linux. Também pode ser bom em PC mais modesto com desktop leve.

## Pontos positivos

- reputação de estabilidade e documentação;
- grande repositório e muitas derivadas;
- escolha de ambientes gráficos;
- bom encaixe para aprender APT e administração tradicional.

## Pontos de atenção

- versões de alguns programas podem ser mais conservadoras;
- firmware/driver pode exigir leitura adicional conforme hardware;
- menos “pronto para jogos” que distribuições especializadas.

## Para quem recomendo / não recomendo

**Recomendo** para quem valoriza estabilidade, servidor, aprendizado de base Debian ou desktop previsível.  
**Não recomendo como primeiro sistema** a quem quer o máximo de automação visual, drivers proprietários simplificados ou versões muito recentes de tudo sem pesquisar.

## Requisitos e desktop

Requisitos variam por arquitetura e ambiente gráfico. Confira a [página oficial](https://www.debian.org/) e escolha GNOME, KDE, Xfce, Cinnamon, MATE ou outro ambiente de acordo com hardware/uso.

## Instalação específica

1. Baixe a ISO somente em [Debian](https://www.debian.org/).
2. Verifique checksum/assinatura conforme [guia oficial](https://www.debian.org/CD/verify).
3. Crie mídia e inicialize em UEFI.
4. Escolha ambiente e opções de firmware somente conforme necessidade do seu hardware.
5. Em dual boot, use apenas espaço não alocado e não formate EFI/Windows existentes.
6. Após iniciar, atualize com o método APT documentado para a versão instalada.

Veja [Instalação geral](./INSTALACAO-GERAL.md) e [Pacotes](../05-pacotes.md).
