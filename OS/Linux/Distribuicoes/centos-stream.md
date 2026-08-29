# CentOS Stream

## Visão geral

| Item | Descrição |
| --- | --- |
| Família/base | Ecossistema Red Hat, posicionado entre Fedora e RHEL no fluxo de desenvolvimento |
| Filosofia | Plataforma de entrega contínua para acompanhar evolução do ecossistema RHEL |
| Dificuldade | 🟡/🔴 |
| Pacotes | RPM/DNF |

## Para que serve

CentOS Stream é útil para desenvolvimento, integração e ambientes que querem acompanhar o fluxo que alimenta futuras atualizações RHEL. Não é sinônimo de clone estável de RHEL nem substituto automático para todo ambiente de produção.

## Pontos positivos

- acesso ao fluxo de desenvolvimento do ecossistema;
- bom para colaborar/testar com tecnologias Red Hat;
- familiaridade com RPM/DNF e ferramentas enterprise.

## Pontos de atenção

- modelo de entrega exige entender expectativa de mudança;
- escolha de produção precisa de política de empresa/suporte;
- não é primeiro sistema desktop para quem só quer simplicidade.

## Para quem recomendo / não recomendo

**Recomendo** para laboratório, desenvolvimento e quem trabalha próximo ao ecossistema Red Hat.  
**Não recomendo** para iniciante desktop ou para produção sem avaliação de ciclo, suporte e compatibilidade.

## Requisitos, desktop e pacotes

Consulte [CentOS Stream](https://www.centos.org/centos-stream/) e documentação atual para imagem/ciclo. Usa RPM/DNF.

## Instalação específica

1. Use mídia oficial da versão/canal escolhido.
2. Prefira VM para entender comportamento de atualização.
3. Planeje repositórios e teste aplicações antes de depender deles.
4. Atualize e monitore serviços/logs desde o primeiro boot.
