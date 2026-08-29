# 01 — Primeiros passos no Linux

## Antes de instalar

Escolha a distribuição conforme seu objetivo, não apenas aparência. Veja a [comparação de distribuições](./Distribuicoes/README.md). Para primeiro contato, live USB ou máquina virtual reduzem risco.

## O que fazer no primeiro dia

1. Atualize o sistema pelo atualizador gráfico ou gerenciador de pacotes da sua distribuição.
2. Confira idioma, teclado, fuso horário e conta de usuário.
3. Teste Wi‑Fi, áudio, Bluetooth, impressora, webcam e monitor.
4. Instale programas pelo repositório/loja oficial primeiro.
5. Configure backup antes de personalizar muito.
6. Aprenda onde ficam seus arquivos: `/home/seu-usuario`.

## Conta normal, root e sudo

Use conta normal para navegar, estudar e criar arquivos. Quando um comando pedir `sudo`, leia o que ele fará. `sudo` não é um prefixo mágico: ele pode alterar o sistema inteiro.

❌ Evite: copiar comandos com `sudo` sem entender.  
✅ Prefira: ler a explicação, verificar o pacote/caminho e perguntar quando o efeito não estiver claro.

## Instalar aplicativos

A ordem de preferência costuma ser:

1. repositório oficial da distribuição;
2. loja gráfica que usa os repositórios/Flatpak configurados;
3. site oficial do projeto, seguindo instrução específica da sua distribuição;
4. AppImage/Snap/Flatpak quando apropriado e confiável.

Não baixe scripts de instalação aleatórios para “resolver dependências”. Consulte [Pacotes](./05-pacotes.md).

## Atualizações

Atualize regularmente. Leia a tela se ela pedir reinicialização, mudança de configuração, substituição de arquivo ou remoção de pacote. Em sistemas de produção, use janela de manutenção e backup; em desktop pessoal, mantenha energia estável e espaço em disco.

## Exercício 🟢

1. Abra o gerenciador de arquivos e localize sua pasta pessoal.
2. Crie uma pasta chamada `linux-pratica`.
3. Abra o terminal nessa pasta, ou navegue até ela com `cd`.
4. Execute `pwd` e `ls`.
5. Atualize somente pelo método documentado para sua distribuição.

Próximo: [Sistema de arquivos](./02-sistema-de-arquivos.md).
