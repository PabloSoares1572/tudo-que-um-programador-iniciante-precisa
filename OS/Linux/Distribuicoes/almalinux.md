# AlmaLinux

## Visão geral

| Item | Descrição |
| --- | --- |
| Família/base | Ecossistema compatível com RHEL |
| Filosofia | Linux empresarial comunitário para servidores, cloud e laboratórios |
| Dificuldade | 🟡 |
| Pacotes | RPM/DNF |

## Para que serve

AlmaLinux é apropriado para administrar servidores e aprender o ecossistema RPM/DNF próximo a RHEL. Pode ser usado em desktop, mas esse não é seu principal diferencial.

## Pontos positivos

- orientação a estabilidade e uso empresarial;
- boa escolha para laboratório de administração;
- ecossistema familiar para ambientes RHEL-like.

## Pontos de atenção

- não assume foco em jogos, drivers proprietários ou desktop pronto;
- versões conservadoras são decisão de estabilidade;
- avalie suporte oficial de aplicações antes de produção.

## Para quem recomendo / não recomendo

**Recomendo** para VM, servidor e estudo de administração empresarial.  
**Não recomendo** como primeira experiência Linux gráfica se seu objetivo é apenas migrar do Windows para jogos/uso doméstico.

## Requisitos, desktop e pacotes

Veja [AlmaLinux](https://almalinux.org/) e documentação atual. Use RPM/DNF e repositórios compatíveis aprovados pelo ambiente.

## Instalação específica

1. Baixe imagem oficial e escolha arquitetura apropriada.
2. Faça instalação de laboratório em VM primeiro.
3. Para servidor, configure rede, hostname, usuário administrador, armazenamento e backup de forma planejada.
4. Atualize após boot e restrinja serviços/portas antes de expor à rede.
