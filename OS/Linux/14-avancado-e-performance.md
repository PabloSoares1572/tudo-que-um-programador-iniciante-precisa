# 14 — Linux avançado e performance

> 🔴/⚫ Estes temas pedem laboratório, backup e documentação específica da distribuição.

## O que estudar depois da base

- processo de boot: UEFI, bootloader, kernel e initramfs;
- kernel e módulos;
- systemd, unidades, timers e logs;
- cgroups e namespaces;
- LVM, RAID, snapshots e filesystems;
- performance de CPU, RAM, I/O e rede;
- compilação e dependências;
- virtualização e containers;
- recuperação e análise de incidentes.

## Performance: medir antes de “otimizar”

| Recurso | Pergunta | Ferramentas de observação |
| --- | --- | --- |
| CPU | Qual processo usa CPU e por quê? | `top`, `htop`, logs, profiler apropriado |
| RAM | Há pressão de memória/swap? | `free`, monitor do sistema, métricas |
| Disco | É latência, espaço, I/O ou erro? | `df`, `lsblk`, logs, ferramentas de I/O |
| Rede | É DNS, rota, perda ou servidor? | `ip`, `ss`, `ping`, `curl`, logs |
| Boot | Qual serviço atrasa inicialização? | ferramentas/relatórios da sua distribuição |

Não desative serviços aleatoriamente para reduzir alguns segundos de boot. Primeiro identifique o serviço, dependências, impacto e ganho mensurável.

## zram, swap, TRIM e bateria

Esses tópicos dependem de hardware, distribuição e carga. zram pode ajudar em certas situações de RAM limitada; swap não é automaticamente “ruim”; TRIM deve seguir suporte do SSD/arquivo de sistema; ajustes de energia em notebook exigem medição de autonomia/temperatura. Leia documentação atual, mude uma coisa e compare antes/depois.

## Especialista é saber recuperar

Antes de um experimento avançado, tenha: backup, live USB, snapshot/VM, acesso ao firmware, documentação oficial e plano de rollback. Fazer boot, rede, logs e dados voltarem é mais importante que ter muitos tweaks.
