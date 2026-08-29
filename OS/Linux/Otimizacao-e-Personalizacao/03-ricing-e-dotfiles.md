# Ricing, dotfiles e configurações

## O que é ricing?

“Ricing” é personalização estética/funcional profunda: terminal, barra, launcher, notificações, atalho, compositor, fontes, cores e gerenciamento de janelas. É criatividade, não requisito para aprender Linux.

## Dotfiles

Dotfiles são arquivos de configuração que frequentemente começam com ponto, como `.bashrc`, `.config/` e `.gitconfig`. Eles são parte importante do seu ambiente e podem conter caminhos, tokens ou dados sensíveis.

## Backup antes de alterar

1. Liste arquivo original e localização.
2. Faça cópia com data em pasta segura.
3. Use Git apenas para configurações sem segredos.
4. Documente dependências: tema, fonte, pacote, extensão e versão.
5. Teste em usuário/VM antes de aplicar no ambiente principal.

## Componentes comuns

- shell e prompt;
- terminal;
- Waybar/painel;
- launchers;
- daemon de notificações;
- compositor;
- gerenciador de janelas;
- atalhos;
- tema/ícones/fontes.

> ⚠️ Não clone dotfiles de terceiros e execute script de instalação sem ler. Eles podem alterar arquivos, instalar pacotes, mudar shell ou sobrescrever configurações. Faça revisão manual e adapte por partes.
