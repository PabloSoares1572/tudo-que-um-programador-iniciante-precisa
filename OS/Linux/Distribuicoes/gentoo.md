# Gentoo

## Visão geral

| Item | Descrição |
| --- | --- |
| Família/base | Gentoo, independente |
| Filosofia | Controle, compilação/configuração e documentação detalhada |
| Lançamento | Rolling, com abordagem source-based em muitos cenários |
| Dificuldade | 🔴/⚫ |
| Pacotes | Portage (`emerge`) |

## Para que serve

Gentoo é excelente como laboratório para entender compilação, USE flags, kernel, init e dependências. A instalação/atualização pode exigir tempo considerável e leitura cuidadosa.

## Pontos positivos

- alto nível de personalização;
- aprendizado profundo de componentes;
- Portage e USE flags dão controle explícito de recursos.

## Pontos de atenção

- curva e tempo de manutenção altos;
- compilação consome CPU/energia/tempo;
- não é solução prática para quem só quer desktop pronto imediatamente.

## Para quem recomendo / não recomendo

**Recomendo** para usuário experiente ou VM de aprendizado.  
**Não recomendo** como primeiro sistema, PC de trabalho sem tempo de manutenção ou servidor crítico sem prática.

## Requisitos, desktop e pacotes

Use [Gentoo](https://www.gentoo.org/) e o Handbook correspondente a arquitetura/init. Portage usa `emerge`; não copie flags ou perfis de outra máquina sem entender.

## Instalação específica

1. Pratique primeiro em VM com snapshot.
2. Leia todo Handbook antes de particionar/compilar.
3. Escolha profile, init, kernel e flags de forma consciente.
4. Registre mudanças e mantenha boot de recuperação.
5. Atualize conforme o processo Portage/Handbook e faça backup antes de alterações grandes.
