# Fedora Atomic Desktops — Silverblue e Kinoite

## Visão geral

| Item | Descrição |
| --- | --- |
| Família/base | Fedora Atomic |
| Filosofia | Desktop imutável/atômico com atualizações transacionais |
| Variantes | Silverblue (GNOME), Kinoite (KDE) e outras variantes oficiais conforme projeto |
| Dificuldade | 🟡/🔴 |
| Pacotes | Base gerenciada de forma atômica; aplicativos normalmente via Flatpak e camadas conforme documentação |

## Para que serve

É interessante para quem quer sistema desktop com atualizações reversíveis e separação maior entre base e aplicativos. Não é “Fedora comum com visual diferente”: o modo de instalar software e modificar o sistema muda.

## Pontos positivos

- atualizações transacionais e possibilidade de rollback;
- bom uso de Flatpak para aplicativos desktop;
- base consistente para desenvolvimento com containers/ferramentas próprias.

## Pontos de atenção

- alguns tutoriais tradicionais de `dnf` não se aplicam da mesma forma;
- camadas na base e alterações manuais precisam ser planejadas;
- exige mudança de mentalidade para personalização/administração.

## Para quem recomendo / não recomendo

**Recomendo** para usuário que quer estabilidade operacional, rollback e entende o modelo atômico.  
**Não recomendo** como primeiro Linux se você quer seguir qualquer tutorial tradicional sem adaptar ou precisa modificar base constantemente.

## Requisitos, desktop e pacotes

Comece pela página de [Fedora Atomic Desktops](https://fedoraproject.org/atomic-desktops/). Confirme variante, hardware, política de aplicativos e método de atualização no guia atual.

## Instalação específica

1. Escolha Silverblue/Kinoite pela interface preferida, não por suposta diferença de desempenho.
2. Baixe imagem oficial e verifique integridade.
3. Teste live USB e boot UEFI antes de instalar.
4. Após instalar, aprenda primeiro atualização/rollback e Flatpak.
5. Em dual boot, aplique as mesmas regras de preservação de Windows/EFI e documente como escolher cada sistema no boot.
