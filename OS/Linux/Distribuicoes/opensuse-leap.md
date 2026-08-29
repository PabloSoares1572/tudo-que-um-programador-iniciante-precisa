# openSUSE Leap

## Visão geral

| Item | Descrição |
| --- | --- |
| Família/base | openSUSE/SUSE |
| Filosofia | Plataforma estável com ferramentas de administração e integração com ecossistema SUSE |
| Lançamento | Mais conservador que Tumbleweed; confirme ciclo atual |
| Dificuldade | 🟡 |
| Pacotes | RPM e Zypper; YaST como ferramenta administrativa importante |

## Para que serve

Leap é voltado a desktop/servidor estável, usuários que querem YaST e ecossistema SUSE. É diferente de Tumbleweed, que prioriza atualização contínua.

## Pontos positivos

- ferramentas YaST para administração;
- base RPM/Zypper;
- foco em estabilidade e integração com SUSE/openSUSE.

## Pontos de atenção

- nomes, modelos de lançamento e suporte podem mudar; confira site oficial;
- documentação de pacote/serviço difere de APT/Pacman;
- não misture repositórios de Leap/Tumbleweed/SLES sem compatibilidade confirmada.

## Para quem recomendo / não recomendo

**Recomendo** para quem busca desktop/servidor estável e quer aprender YaST/Zypper.  
**Não recomendo** para quem precisa das versões mais novas de tudo ou quer primeiro Linux com o máximo de tutoriais Ubuntu.

## Requisitos, desktop e pacotes

Veja [openSUSE](https://get.opensuse.org/) para disponibilidade atual, requisitos e edições. Zypper gerencia RPM; YaST ajuda em configuração, mas não substitui backup/conhecimento.

## Instalação específica

1. Baixe a imagem Leap oficial se ela estiver disponível para seu cenário.
2. Teste mídia, UEFI e hardware em modo live/instalador.
3. Leia resumo de particionamento e proposta de filesystem antes de aceitar.
4. Em dual boot, preserve Windows/ESP e use espaço livre planejado.
5. Atualize com Zypper e acompanhe notas do projeto.
