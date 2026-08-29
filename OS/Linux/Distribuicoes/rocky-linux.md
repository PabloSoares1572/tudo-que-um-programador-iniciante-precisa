# Rocky Linux

## Visão geral

| Item | Descrição |
| --- | --- |
| Família/base | Ecossistema compatível com RHEL |
| Filosofia | Plataforma comunitária para servidores e ambientes empresariais |
| Dificuldade | 🟡 |
| Pacotes | RPM/DNF |

## Para que serve

Rocky Linux é usado em cenários de servidor, laboratórios e infraestrutura que procuram compatibilidade com ecossistema RHEL sem usar necessariamente uma assinatura RHEL direta. Confirme compatibilidade e suporte para cada software/empresa.

## Pontos positivos

- ciclo e foco próximos a ambiente empresarial;
- comunidade e documentação próprias;
- bom para estudar ferramentas RPM/DNF, serviços e servidores.

## Pontos de atenção

- não é pensado primeiro para desktop gamer;
- pacote conservador pode exigir estratégia diferente para software muito novo;
- “compatível” não substitui teste/certificação exigida por fornecedor.

## Para quem recomendo / não recomendo

**Recomendo** para VM/servidor de estudo e cenários RHEL-like.  
**Não recomendo** como primeira distro desktop se o objetivo é jogos ou interface pronta para consumo.

## Requisitos, desktop e pacotes

Confira [Rocky Linux](https://rockylinux.org/) para imagens, arquiteturas e notas atuais. O gerenciamento de pacotes usa RPM/DNF.

## Instalação específica

1. Baixe ISO no portal/mirror oficial indicado.
2. Use VM para aprender Anaconda, rede, partições e serviços antes de servidor real.
3. Em produção, planeje hostname, IP, usuários, SSH, firewall, atualizações e backup antes da instalação.
4. Depois do primeiro boot, aplique updates e confirme logs/serviços básicos.
