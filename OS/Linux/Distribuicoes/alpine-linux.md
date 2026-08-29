# Alpine Linux

## Visão geral

| Item | Descrição |
| --- | --- |
| Família/base | Alpine, independente |
| Filosofia | Sistema pequeno, simples e focado em segurança/containers/servidores |
| Dificuldade | 🔴 para desktop tradicional |
| Pacotes | APK |

## Para que serve

Alpine é muito usado em containers, appliances e servidores compactos. Não é escolha padrão para desktop de iniciante, pois usa componentes/decisões diferentes de distribuições GNU/Linux tradicionais em alguns aspectos.

## Pontos positivos

- imagem pequena e boa para containers;
- foco em simplicidade e segurança;
- APK é rápido e direto.

## Pontos de atenção

- compatibilidade de software/binários pode diferir devido a escolhas de biblioteca/componentes;
- desktop e drivers podem exigir mais esforço;
- “leve” não significa automaticamente adequado para todo PC/usuário.

## Para quem recomendo / não recomendo

**Recomendo** para containers, laboratório de servidor e quem entende o objetivo.  
**Não recomendo** como primeiro desktop/gaming ou substituto universal de Ubuntu/Fedora.

## Requisitos, desktop e pacotes

Consulte [Alpine Linux](https://alpinelinux.org/) e wiki/documentação oficial. O gerenciador é `apk`; siga o guia específico de sua arquitetura/cenário.

## Instalação específica

1. Prefira VM/container para primeiro contato.
2. Baixe imagem oficial para arquitetura correta.
3. Leia procedimento de instalação/configuração de rede antes de instalar em máquina física.
4. Para servidor, planeje usuários, SSH, firewall, atualizações e backup.
5. Não trate comandos/configuração de Debian como equivalentes no Alpine.
