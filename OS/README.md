# Enciclopédia prática de Sistemas Operacionais

Esta é uma base de conhecimento em português brasileiro sobre **Windows, Linux, instalação, manutenção, dual boot, segurança e administração de sistemas**. Ela começa no nível zero e avança com cuidado até tópicos profissionais.

> 🟢 **Comece devagar.** Em assuntos de disco, boot, criptografia e permissões, entender o passo é mais importante do que copiar um comando.

## O que é um sistema operacional?

O sistema operacional (SO) é o software principal do computador. Ele faz a ponte entre você, os programas e o hardware: inicializa a máquina, gerencia memória, discos, rede, contas de usuário, periféricos e segurança.

Sem um SO, o navegador, o jogo, o editor de texto e os drivers não têm uma base organizada para funcionar.

## Windows x Linux em uma tabela

| Tema | Windows | Linux |
| --- | --- | --- |
| Modelo | Produto da Microsoft com edições comerciais | Ecossistema de distribuições de código aberto |
| Compatibilidade de programas | Muito ampla para softwares e jogos comerciais | Muito ampla para desenvolvimento; alguns programas/jogos exigem alternativa ou camada de compatibilidade |
| Instalação | Fluxo padronizado pela Microsoft e fabricantes | Varia conforme a distribuição e o instalador |
| Personalização | Boa, com limites definidos pela edição | Pode ir de simples a extremamente profunda |
| Administração | Ferramentas gráficas, Terminal e PowerShell | Terminal e ferramentas de administração fazem parte do uso comum |
| Melhor escolha | Depende de compatibilidade, suporte e necessidade | Depende de objetivo, hardware e disposição para aprender |

Nenhum é “melhor para tudo”. A escolha certa depende do programa que você usa, do hardware, do tempo para aprender e do nível de controle desejado.

## Como usar esta documentação

1. Leia primeiro os conceitos e avisos de segurança.
2. Faça backup antes de qualquer alteração em disco ou boot.
3. Siga os links internos em vez de pular para comandos avançados.
4. Use comandos em exemplos pequenos e verifique a saída antes de continuar.
5. Para downloads, versões, suporte e requisitos, confira as [referências oficiais](./REFERENCIAS-OFICIAIS.md) na data em que for executar a tarefa.

## Comece aqui

| Se você quer… | Leia primeiro |
| --- | --- |
| Entender seu computador | [Glossário](./GLOSSARIO.md) e esta página |
| Reinstalar sem perder dados | [Formatar o PC](./FORMATAR-PC.md) |
| Usar Windows e Linux no mesmo PC | [Dual boot](./DUAL-BOOT.md) |
| Experimentar Linux pela primeira vez | [Linux — Comece aqui](./Linux/README.md) |
| Aprender terminal de verdade | [Curso de terminal](./Linux/03-Terminal/README.md) |
| Escolher uma distribuição | [Comparação de distribuições](./Linux/Distribuicoes/README.md) |
| Escolher Windows e edição adequados | [Windows — Comece aqui](./Windows/README.md) |

## Caminhos de aprendizagem

### 🟢 Usuário iniciante

1. [FORMATAR-PC](./FORMATAR-PC.md) — apenas as partes de backup e conceitos.
2. [Windows ou Linux?](./Windows/02-escolher-windows.md) e [O que é Linux?](./Linux/00-o-que-e-linux.md).
3. [Primeiros passos no Linux](./Linux/01-primeiros-passos.md).
4. [Distribuições](./Linux/Distribuicoes/README.md).

### 🟡 Usuário de Linux

1. [Sistema de arquivos](./Linux/02-sistema-de-arquivos.md).
2. [Terminal](./Linux/03-Terminal/README.md).
3. [Usuários e permissões](./Linux/04-usuarios-e-permissoes.md).
4. [Pacotes](./Linux/05-pacotes.md), [processos](./Linux/06-processos-e-servicos.md) e [rede](./Linux/08-rede.md).

### 🔴 Administração e carreira

1. [Roadmap Linux](./ROADMAP-LINUX.md).
2. [Administração e armazenamento](./Linux/11-administracao-e-armazenamento.md).
3. [Servidores, containers e virtualização](./Linux/12-servidores-containers-e-virtualizacao.md).
4. [Shell e automação](./Linux/10-shell-e-scripts.md).
5. [Segurança](./Linux/09-seguranca.md) e [troubleshooting](./Linux/13-troubleshooting.md).

## Índice geral

### Guias gerais

- [Formatar um PC com segurança](./FORMATAR-PC.md)
- [Dual boot Windows + Linux](./DUAL-BOOT.md)
- [Glossário](./GLOSSARIO.md)
- [Roadmap: do zero à administração Linux](./ROADMAP-LINUX.md)
- [Referências oficiais e política de atualização](./REFERENCIAS-OFICIAIS.md)

### Windows

- [Página inicial Windows](./Windows/README.md)
- [Versões e edições](./Windows/01-versoes-e-edicoes.md)
- [Qual Windows escolher](./Windows/02-escolher-windows.md)
- [Instalação e reinstalação](./Windows/03-instalacao-e-reinstalacao.md)
- [Atualizações, drivers e ativação legítima](./Windows/04-atualizacoes-drivers-e-ativacao.md)
- [Otimização realista](./Windows/05-otimizacao.md)
- [Segurança](./Windows/06-seguranca.md)
- [Troubleshooting](./Windows/07-troubleshooting.md)

### Linux

- [Página inicial Linux](./Linux/README.md)
- [Fundamentos](./Linux/00-o-que-e-linux.md)
- [Primeiros passos](./Linux/01-primeiros-passos.md)
- [Sistema de arquivos](./Linux/02-sistema-de-arquivos.md)
- [Terminal](./Linux/03-Terminal/README.md)
- [Usuários e permissões](./Linux/04-usuarios-e-permissoes.md)
- [Pacotes](./Linux/05-pacotes.md)
- [Processos e serviços](./Linux/06-processos-e-servicos.md)
- [Discos e partições](./Linux/07-discos-e-particoes.md)
- [Rede](./Linux/08-rede.md)
- [Segurança](./Linux/09-seguranca.md)
- [Shell e scripts](./Linux/10-shell-e-scripts.md)
- [Administração e armazenamento](./Linux/11-administracao-e-armazenamento.md)
- [Servidores, containers e virtualização](./Linux/12-servidores-containers-e-virtualizacao.md)
- [Troubleshooting](./Linux/13-troubleshooting.md)
- [Avançado e performance](./Linux/14-avancado-e-performance.md)
- [Distribuições](./Linux/Distribuicoes/README.md)
- [Otimização e personalização](./Linux/Otimizacao-e-Personalizacao/README.md)
- [Cheat sheets](./Linux/Cheat-Sheets/README.md)

## Convenções de segurança

- 🟢 **Iniciante:** pode praticar em conta normal, com atenção.
- 🟡 **Intermediário:** faça backup e entenda os pré-requisitos.
- 🔴 **Avançado:** use máquina virtual, ambiente de teste ou plano de reversão.
- ⚫ **Especialista:** envolve infraestrutura, criptografia, boot, discos ou produção.

> ⚠️ **ATENÇÃO:** um comando não é uma instrução universal. Verifique nome do disco, caminho, distribuição, versão e contexto antes de executar.
