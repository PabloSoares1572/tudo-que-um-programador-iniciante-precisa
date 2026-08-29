# Distribuições Linux — comparação e escolha

## Antes de escolher

Uma distribuição é uma combinação de base, repositórios, instalador, atualizações, ambiente gráfico e comunidade. Não existe “a melhor Linux” universal; existe a melhor para um cenário, hardware e disposição para aprender.

> **Atualização:** não congele versão, requisito ou suporte nesta página. Abra o site oficial da distribuição no dia da instalação e confira a documentação da edição escolhida.

## Comparação rápida

| Distribuição/família | Iniciante | Jogos | Programação | Servidor | PC antigo | Privacidade | Dificuldade |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Ubuntu | Alta | Boa | Alta | Alta | Média | Média | 🟢 |
| Linux Mint | Muito alta | Boa | Boa | Baixa | Boa com Xfce | Média | 🟢 |
| Zorin OS | Muito alta | Boa | Boa | Baixa | Boa com edição adequada | Média | 🟢 |
| Fedora | Média/alta | Boa | Alta | Alta | Média | Média | 🟡 |
| Debian | Média | Boa | Alta | Muito alta | Boa | Média | 🟡 |
| openSUSE Leap/Tumbleweed | Média | Boa | Alta | Alta | Média | Média | 🟡 |
| Arch | Baixa para primeiro sistema | Boa | Alta | Baixa sem experiência | Média | Média | 🔴 |
| EndeavourOS | Média | Boa | Alta | Baixa | Média | Média | 🟡/🔴 |
| Bazzite | Média | Muito alta | Média | Não é foco | Média | Média | 🟡 |
| RHEL/Rocky/Alma | Baixa para desktop comum | Baixa | Alta | Muito alta | Média | Média | 🟡 |
| Alpine | Baixa | Baixa | Média | Alta em casos específicos | Alta | Alta | 🔴 |
| NixOS | Baixa | Boa | Alta | Média | Média | Média | 🔴 |
| Tails | Não é desktop diário | Não | Não é foco | Não | Média | Muito alta | 🟡 |
| Qubes OS | Não para iniciante | Não é foco | Alta para segurança | Não é foco | Baixa | Muito alta | 🔴 |
| SteamOS | Foco em Steam Deck/hardware suportado | Muito alta | Média | Não | Baixa | Média | 🟡 |

Essa tabela é orientação, não promessa. Compatibilidade de jogo, hardware e aplicativos deve ser testada no seu caso.

## Recomendações por objetivo

### Melhor Linux para iniciantes

**Linux Mint, Zorin OS e Ubuntu** são pontos de partida frequentes por instaladores amigáveis, comunidade e documentação. Escolha a interface/edição que o seu hardware suporta e teste por live USB quando possível.

### Melhor Linux para jogos

**Bazzite** é voltado a experiência de jogos em cenários compatíveis; **Fedora**, **Ubuntu**, **Linux Mint**, **Arch/derivadas** também podem funcionar bem. A escolha depende de GPU, jogo, anti-cheat, Steam/Proton e sua vontade de administrar o sistema. Não compre ou formate PC supondo compatibilidade sem verificar os jogos que você realmente joga.

### Melhor Linux para programadores

**Ubuntu, Fedora, Debian, openSUSE, Arch e NixOS** têm bons ecossistemas, com trade-offs entre estabilidade, versões novas e curva de aprendizado. Comece pelo sistema que permite trabalhar sem transformar cada atualização em projeto.

### Melhor Linux para servidor

**Debian, Ubuntu Server, RHEL, Rocky Linux, AlmaLinux e SLES** são referências frequentes. Em produção, escolha pelo suporte, ciclo de vida, documentação, compatibilidade de software e política da empresa — não pelo visual.

### Melhor Linux para notebook / PC fraco

Considere **Linux Mint Xfce**, **Zorin Lite quando disponível**, **Xfce/MATE**, **MX Linux**, **antiX**, **Puppy Linux** ou distribuição leve escolhida com cuidado. PC muito antigo pode ter limitação de arquitetura, Wi‑Fi, GPU ou navegador moderno; teste live USB.

### Melhor Linux para aprender profundamente

**Arch** e **Gentoo** ensinam muitos componentes, mas têm custo de tempo e exigem leitura. Para aprender sem usar como sistema principal, prefira VM e siga documentação oficial.

### Melhor para privacidade/segurança

**Tails** e **Qubes OS** têm objetivos específicos e não são substitutos universais de desktop. Use somente depois de entender modelo de ameaça, requisitos e limitações. **Kali** e **Parrot** não são “mais seguros” por serem ferramentas de pentest.

## Índice de páginas próprias

### Debian e derivadas

- [Debian](./debian.md)
- [Ubuntu](./ubuntu.md)
- [Linux Mint](./linux-mint.md)
- [Pop!_OS](./pop-os.md)
- [Zorin OS](./zorin-os.md)
- [elementary OS](./elementary-os.md)
- [Kali Linux](./kali-linux.md)
- [Parrot OS](./parrot-os.md)
- [MX Linux](./mx-linux.md)
- [antiX](./antix.md)

### Fedora e RHEL

- [Fedora Linux](./fedora.md)
- [Fedora Atomic Desktops — Silverblue/Kinoite](./fedora-atomic.md)
- [Nobara](./nobara.md)
- [Bazzite](./bazzite.md)
- [RHEL](./rhel.md)
- [Rocky Linux](./rocky-linux.md)
- [AlmaLinux](./almalinux.md)
- [CentOS Stream](./centos-stream.md)

### Arch e derivadas

- [Arch Linux](./arch-linux.md)
- [Manjaro](./manjaro.md)
- [EndeavourOS](./endeavouros.md)
- [CachyOS](./cachyos.md)
- [Garuda Linux](./garuda-linux.md)

### Outras famílias e especializadas

- [openSUSE Leap](./opensuse-leap.md)
- [openSUSE Tumbleweed](./opensuse-tumbleweed.md)
- [SUSE Linux Enterprise](./suse-linux-enterprise.md)
- [Gentoo](./gentoo.md)
- [Alpine Linux](./alpine-linux.md)
- [NixOS](./nixos.md)
- [Void Linux](./void-linux.md)
- [Slackware](./slackware.md)
- [Solus](./solus.md)
- [Puppy Linux](./puppy-linux.md)
- [Tails](./tails.md)
- [Qubes OS](./qubes-os.md)
- [SteamOS](./steamos.md)

## Instalação

Leia primeiro [Instalação geral de distribuições](./INSTALACAO-GERAL.md). Cada página específica traz foco, pacotes, pontos de atenção e fonte oficial da ISO.
