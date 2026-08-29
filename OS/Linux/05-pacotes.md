# 05 — Gerenciadores de pacotes

## O que é pacote?

Pacote é uma unidade de software com arquivos, metadados e dependências. O gerenciador instala, atualiza e remove de maneira rastreável a partir de repositórios configurados.

## Ecossistemas principais

| Família | Gerenciador | Atualização típica | Instalação típica |
| --- | --- | --- | --- |
| Debian/Ubuntu | APT | `sudo apt update` + `sudo apt upgrade` | `sudo apt install pacote` |
| Fedora/RHEL | DNF | `sudo dnf upgrade --refresh` | `sudo dnf install pacote` |
| Arch | Pacman | `sudo pacman -Syu` | `sudo pacman -S pacote` |
| openSUSE | Zypper | `sudo zypper refresh` + `sudo zypper update` | `sudo zypper install pacote` |
| Alpine | APK | `sudo apk update` + `sudo apk upgrade` | `sudo apk add pacote` |
| Gentoo | Portage | sincronizar e atualizar conforme handbook | `emerge --ask pacote` |

> ⚠️ Os comandos da tabela são exemplos de família, não ordem para colar sem confirmar distribuição, versão e documentação. Em especial, Arch deve ser atualizado como sistema inteiro, não por atualizações parciais.

## Formatos alternativos

| Formato | Ideia | Pontos fortes | Cuidados |
| --- | --- | --- | --- |
| Pacote tradicional | Integrado ao repositório da distro | Integração e atualizações centralizadas | Pode ter versão mais conservadora |
| Flatpak | Aplicação isolada com runtimes | Bom para desktop e versões independentes | Ocupa espaço e permissões devem ser revisadas |
| Snap | Pacotes confinados com canal próprio | Atualização e empacotamento simplificados | Integração/experiência varia por distro/app |
| AppImage | Arquivo executável portátil | Não exige instalação tradicional | Atualização e confiança ficam por sua conta |

## Regras de ouro

1. Atualize índices/repositórios pelo método oficial.
2. Instale de fonte conhecida e confira nome do pacote.
3. Leia o que será instalado/removido antes de confirmar.
4. Evite misturar repositórios de versões/famílias diferentes.
5. Nunca rode script `curl ... | sudo sh` sem auditar origem e conteúdo.

## Exercício 🟢

Abra a documentação da sua distribuição, descubra qual é seu gerenciador de pacotes e localize o comando de **consulta** de pacote sem instalar nada. Depois pesquise uma aplicação conhecida na loja/repositório oficial.
