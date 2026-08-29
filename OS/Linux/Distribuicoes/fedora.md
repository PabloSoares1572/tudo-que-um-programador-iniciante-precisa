# Fedora Linux

## Visão geral

| Item | Descrição |
| --- | --- |
| Família/base | Fedora, independente; upstream importante para ecossistema Red Hat |
| Filosofia | Software livre, tecnologias atuais e boa integração desktop/servidor |
| Lançamento | Ciclo regular com versões mais recentes que distribuições conservadoras |
| Dificuldade | 🟡 |
| Pacotes | RPM e DNF |

## Para que serve

Fedora funciona bem para desktop, desenvolvimento, programação, estações de trabalho e aprendizado de tecnologias modernas. Também possui edições para servidor, cloud e desktops alternativos.

## Pontos positivos

- tecnologias e kernels relativamente atuais;
- boa documentação e comunidade;
- edições para GNOME, KDE Plasma, servidor e outros cenários;
- DNF/RPM e conexão com o ecossistema Red Hat.

## Pontos de atenção

- ciclo mais rápido pede atualizações e atenção a mudanças;
- alguns codecs/drivers podem exigir seguir documentação de fontes confiáveis;
- não é a mesma coisa que RHEL em ciclo, suporte e finalidade.

## Para quem recomendo / não recomendo

**Recomendo** para programadores, desktop atual e quem quer aprender RPM/DNF.  
**Não recomendo** para quem quer pacote extremamente conservador por muitos anos ou não pretende manter o sistema atualizado.

## Requisitos, desktop e pacotes

Consulte [Fedora oficial](https://fedoraproject.org/) e a [página de download da Workstation](https://fedoraproject.org/workstation/download/). GNOME é edição conhecida; há KDE e outras opções oficiais. Use `dnf` para pacotes.

## Instalação específica

1. Baixe imagem somente em Fedora e confira checksum/assinatura conforme o projeto.
2. A documentação recomenda mídia de boot apropriada; grave em pendrive correto e teste live.
3. Escolha edição (Workstation/KDE/Server) conforme objetivo, não só aparência.
4. Em dual boot, use espaço não alocado e preserve a ESP Windows conforme [Dual boot](../../DUAL-BOOT.md).
5. Após boot, atualize com DNF e configure drivers pelo caminho recomendado para Fedora.
