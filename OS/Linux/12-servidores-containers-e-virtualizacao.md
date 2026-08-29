# 12 — Servidores, containers e virtualização

## Servidor não é só “Linux sem interface”

Um servidor entrega serviço a outras máquinas: web, banco, arquivos, identidade, DNS, monitoramento ou aplicação. Administração exige atualização, acesso remoto seguro, logs, backup, firewall e documentação.

## SSH

SSH é base do acesso remoto. Boas práticas: usuário normal, autenticação por chave, senha forte/MFA quando disponível, atualização, firewall, logs e política de quem pode entrar. Não exponha servidor de teste à internet sem entender as consequências.

## Virtualização

Máquina virtual emula/abstrai computador completo. É ótima para laboratório, isolamento e snapshots. Ela consome RAM, CPU e armazenamento; host e guest precisam ser atualizados.

## Containers

Containers empacotam aplicação e dependências, compartilhando kernel do host. Docker e Podman são tecnologias comuns. Eles não substituem política de atualização, segredo, rede, backup ou revisão de imagem.

| Tecnologia | Isolamento | Uso típico |
| --- | --- | --- |
| Máquina virtual | SO completo separado | Laboratório, sistemas diferentes, isolamento maior |
| Container | Processo isolado no mesmo kernel | Serviços reprodutíveis e deploy de aplicações |

## Princípios de produção

- Imagem mínima e de fonte confiável.
- Versões declaradas e atualizadas.
- Segredos fora da imagem e repositório.
- Portas mínimas expostas.
- Volumes/backups documentados.
- Logs e métricas observáveis.
- Teste de atualização/rollback.

## Exercício 🟡

Monte VM Linux sem dados sensíveis. Pratique snapshot, atualização, acesso por rede interna e restauração de snapshot. Só depois explore containers.
