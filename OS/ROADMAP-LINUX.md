# Roadmap: de “nunca usei Linux” à administração profissional

Este roadmap não é uma prova. Avance quando você conseguir realizar as tarefas do nível sem copiar passos cegamente.

## Nível 0 — Primeiro contato 🟢

**Domine:** o que é Linux, distribuição, live USB, desktop e conta de usuário.  
**Pratique:** testar uma distribuição em máquina virtual ou live USB, abrir configurações e desligar corretamente.  
**Leia:** [O que é Linux](./Linux/00-o-que-e-linux.md) e [Primeiros passos](./Linux/01-primeiros-passos.md).

## Nível 1 — Usuário Linux 🟢

**Domine:** instalar programas por interface, atualizar, reconhecer arquivos, periféricos e ambiente gráfico.  
**Pratique:** instalar uma aplicação de repositório oficial, criar documentos, atualizar sistema e consultar ajuda.  
**Avance quando:** souber explicar a diferença entre arquivo, pasta, pacote e repositório.

## Nível 2 — Terminal 🟢

**Domine:** `pwd`, `ls`, `cd`, `mkdir`, `cp`, `mv`, `less`, `head`, `tail` e ajuda (`man`, `--help`).  
**Pratique:** criar estrutura de pastas, copiar com confirmação e localizar arquivos.  
**Leia:** [Curso de terminal](./Linux/03-Terminal/README.md).

## Nível 3 — Administração básica 🟡

**Domine:** usuários, grupos, `sudo`, permissões, atualização, processos e serviços.  
**Pratique:** criar usuário de teste, ajustar permissões em arquivos próprios e investigar serviço com `systemctl status`.  
**Leia:** [Permissões](./Linux/04-usuarios-e-permissoes.md), [Pacotes](./Linux/05-pacotes.md) e [Serviços](./Linux/06-processos-e-servicos.md).

## Nível 4 — Administração intermediária 🟡

**Domine:** discos, montagens, logs, backups, processos, inicialização e `fstab`.  
**Pratique:** montar unidade externa, observar `lsblk -f`, ler logs de boot e documentar um procedimento de backup.  
**Leia:** [Discos](./Linux/07-discos-e-particoes.md) e [Administração](./Linux/11-administracao-e-armazenamento.md).

## Nível 5 — Redes e segurança 🟡

**Domine:** IP, gateway, DNS, portas, SSH, firewall, atualizações, menor privilégio e logs.  
**Pratique:** diagnosticar DNS, testar conexão, usar SSH com chave em laboratório e revisar serviços expostos.  
**Leia:** [Rede](./Linux/08-rede.md) e [Segurança](./Linux/09-seguranca.md).

## Nível 6 — Shell e automação 🔴

**Domine:** variáveis, argumentos, condições, loops, funções, códigos de saída, pipes, redirecionamentos e agendamento.  
**Pratique:** script de backup de diretório de teste com logs e validações.  
**Leia:** [Shell e scripts](./Linux/10-shell-e-scripts.md).

## Nível 7 — Servidores 🔴

**Domine:** SSH seguro, serviços, monitoramento, web server, bancos, containers, virtualização e documentação operacional.  
**Pratique:** VM com servidor de teste, firewall restritivo, backup e restauração.  
**Leia:** [Servidores, containers e virtualização](./Linux/12-servidores-containers-e-virtualizacao.md).

## Nível 8 — Troubleshooting avançado 🔴

**Domine:** método de diagnóstico, logs de boot, rede, discos, permissões, performance e recuperação.  
**Pratique:** resolver incidentes simulados sem apagar evidências.  
**Leia:** [Troubleshooting Linux](./Linux/13-troubleshooting.md).

## Nível 9 — Linux avançado ⚫

**Domine:** kernel, módulos, initramfs, boot, LVM, RAID, filesystems, namespaces, cgroups e performance.  
**Pratique:** sempre em laboratório/VM, com snapshots e plano de rollback.  
**Leia:** [Avançado e performance](./Linux/14-avancado-e-performance.md).

## Nível 10 — Administração profissional ⚫

**Domine:** automação versionada, observabilidade, segurança, capacidade, documentação, incidentes, mudança controlada e recuperação testada.  
**Pratique:** criar runbooks, métricas, testes de restauração e revisão pós-incidente.

> Meta profissional: não é “saber todos os comandos”; é diagnosticar com método, documentar decisões, limitar risco e recuperar serviços com segurança.
