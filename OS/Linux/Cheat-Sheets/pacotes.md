# Cheat sheet — Pacotes

| Família | Atualizar | Instalar | Remover |
| --- | --- | --- | --- |
| Debian/Ubuntu | `sudo apt update && sudo apt upgrade` | `sudo apt install pacote` | `sudo apt remove pacote` |
| Fedora/RHEL | `sudo dnf upgrade --refresh` | `sudo dnf install pacote` | `sudo dnf remove pacote` |
| Arch | `sudo pacman -Syu` | `sudo pacman -S pacote` | `sudo pacman -Rns pacote` |
| openSUSE | `sudo zypper refresh && sudo zypper update` | `sudo zypper install pacote` | `sudo zypper remove pacote` |
| Alpine | `sudo apk update && sudo apk upgrade` | `sudo apk add pacote` | `sudo apk del pacote` |

> ⚠️ Confirme sua distribuição. Não misture repositórios nem use atualização parcial em Arch. Leia [Pacotes](../05-pacotes.md).
