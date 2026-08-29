# Void Linux

## Visão geral

| Item | Descrição |
| --- | --- |
| Família/base | Void, independente |
| Filosofia | Simplicidade, rolling release e runit em vez de systemd |
| Dificuldade | 🔴 |
| Pacotes | XBPS |

## Para que serve

Void interessa a usuário que quer sistema independente, leve e diferente do fluxo systemd. É boa oportunidade para entender conceitos de init e administração, mas não deve ser escolhida apenas por curiosidade sem backup/tempo.

## Pontos positivos

- independente e leve;
- runit oferece modelo diferente de serviços;
- XBPS e documentação própria.

## Pontos de atenção

- muitos tutoriais assumem systemd e não se aplicam;
- comunidade/ecossistema menor que Ubuntu/Fedora;
- instalação/administração exigem conforto com terminal.

## Para quem recomendo / não recomendo

**Recomendo** para usuário experiente, laboratório e curiosidade sobre init alternativo.  
**Não recomendo** como primeiro Linux, ambiente corporativo sem suporte ou quem depende de tutorial genérico.

## Requisitos, desktop e pacotes

Use [Void Linux](https://voidlinux.org/) para ISO, arquiteturas e documentação. O gerenciador é XBPS; serviços usam runit.

## Instalação específica

1. Teste em VM antes de tornar sistema principal.
2. Baixe imagem oficial e escolha biblioteca/arquitetura conforme documentação.
3. Leia sobre init/runit e rede antes de instalar servidor.
4. Em dual boot, use espaço livre e preserve entradas EFI existentes.
5. Mantenha documentação Void separada de comandos systemd de outras distros.
