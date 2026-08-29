# Glossário de sistemas operacionais

| Termo | Significado |
| --- | --- |
| BIOS | Firmware mais antigo que inicializa o computador; em PCs atuais, UEFI é mais comum |
| UEFI | Firmware moderno que inicializa sistemas e gerencia entradas de boot |
| Boot | Processo de inicialização do computador |
| Boot Menu | Menu temporário para escolher dispositivo/sistema de inicialização |
| Bootloader | Programa que carrega o sistema; GRUB é comum no Linux |
| EFI / ESP | Partição de sistema EFI, usada pelo UEFI para arquivos de boot |
| Kernel | Parte central do SO que conversa com hardware e gerencia recursos |
| Distro | Distribuição Linux: sistema que reúne kernel, programas, repositórios e configurações |
| Shell | Interpretador de comandos, como Bash ou Zsh |
| Terminal | Aplicativo que oferece uma interface de texto ao shell |
| Root | Conta administrativa máxima no Linux |
| sudo | Executa um comando com privilégios administrativos, mediante permissão |
| Pacote | Unidade instalável de software no gerenciador de pacotes |
| Repositório | Fonte de pacotes e atualizações mantida por projeto/empresa/comunidade |
| Daemon / serviço | Processo que roda em segundo plano e oferece uma função ao sistema |
| Processo | Programa em execução |
| PID | Identificador numérico de um processo |
| Filesystem | Organização de arquivos e diretórios; também pode significar um sistema de arquivos como ext4/NTFS |
| Mount / montar | Tornar um sistema de arquivos acessível em um diretório |
| ISO | Arquivo que representa mídia de instalação |
| Partição | Divisão lógica de um disco físico |
| Volume | Área de armazenamento apresentada ao sistema, frequentemente uma partição formatada |
| GPT | Tabela de partições moderna, usual em sistemas UEFI |
| MBR | Tabela de partições antiga, limitada em comparação com GPT |
| NTFS | Sistema de arquivos comum no Windows |
| FAT32 | Sistema de arquivos compatível, usado em muitas mídias EFI, com limite de arquivo de 4 GB |
| exFAT | Sistema de arquivos simples e compatível para unidades externas |
| ext4 | Sistema de arquivos padrão em muitas distribuições Linux |
| swap | Espaço usado pelo Linux como apoio à memória; arquivo ou partição |
| Secure Boot | Recurso de UEFI que verifica componentes de inicialização compatíveis |
| TPM | Módulo de segurança usado por recursos como criptografia e requisitos do Windows 11 |
| BitLocker | Criptografia de unidade do Windows, disponível conforme edição/configuração |
| LVM | Camada de gerenciamento lógico de volumes no Linux |
| RAID | Técnica que combina discos para redundância, desempenho ou ambos; não substitui backup |
| initramfs | Sistema de arquivos temporário usado no início do boot Linux |
| systemd | Conjunto de componentes de inicialização/serviços usado por muitas distribuições |
| `fstab` | Arquivo que descreve montagens persistentes no Linux |
| SSH | Protocolo seguro de acesso remoto a terminal/arquivos |
| DNS | Sistema que traduz nomes, como `exemplo.com`, em endereços IP |
| DHCP | Serviço que entrega configuração de rede automaticamente |
| Firewall | Regras que controlam tráfego de rede permitido/bloqueado |

Volte a este glossário sempre que aparecer um termo desconhecido. Para aplicação prática, siga os módulos do [Linux](./Linux/README.md) ou [Windows](./Windows/README.md).
