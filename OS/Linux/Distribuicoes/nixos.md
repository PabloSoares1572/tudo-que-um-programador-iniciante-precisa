# NixOS

## Visão geral

| Item | Descrição |
| --- | --- |
| Família/base | NixOS, independente |
| Filosofia | Configuração declarativa e reprodutível com Nix |
| Dificuldade | 🔴 |
| Pacotes | Nix e configuração declarativa |

## Para que serve

NixOS é atraente para desenvolvimento, administração reproduzível e quem quer declarar estado do sistema em arquivos de configuração. Muda bastante a forma de instalar pacotes/alterar sistema em comparação com APT/DNF/Pacman.

## Pontos positivos

- configuração versionável e reproduzível;
- gerações/rollback como parte do modelo;
- útil para ambientes e desenvolvimento declarativos.

## Pontos de atenção

- linguagem/configuração tem curva própria;
- tutoriais tradicionais Linux podem não se aplicar diretamente;
- rollback não substitui backup de dados de usuário.

## Para quem recomendo / não recomendo

**Recomendo** para desenvolvedor/sysadmin que quer infraestrutura/configuração declarativa e aceita estudar Nix.  
**Não recomendo** para primeiro Linux ou usuário que quer instalar/alterar tudo por comandos familiares sem aprender o modelo.

## Requisitos, desktop e pacotes

Consulte [NixOS](https://nixos.org/) e manual atual. Requisitos/desktop são definidos pela imagem e configuração escolhida.

## Instalação específica

1. Comece em VM e mantenha configuração sob versionamento sem segredos.
2. Baixe ISO oficial e leia instalação da release atual.
3. Planeje particionamento, configuração de hardware e arquivo declarativo antes de confirmar instalação.
4. Faça mudanças pequenas, gere nova configuração e aprenda rollback.
5. Não copie `configuration.nix` de terceiros sem auditar usuários, serviços, portas e chaves.
