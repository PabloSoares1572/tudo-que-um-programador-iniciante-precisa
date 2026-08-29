# 08 — Rede no Linux

## Conceitos básicos

| Termo | Explicação |
| --- | --- |
| IP | Endereço de um dispositivo na rede |
| Gateway | Roteador/saída para outras redes |
| DNS | Traduz nomes de domínio em IPs |
| DHCP | Entrega configuração de rede automaticamente |
| localhost | O próprio computador, geralmente `127.0.0.1`/`::1` |
| Porta | Número que identifica serviço de rede em um IP |
| TCP | Protocolo orientado a conexão |
| UDP | Protocolo sem conexão, usado quando baixa latência importa |

## Diagnóstico em ordem

1. A interface de rede aparece? (`ip addr`)
2. Recebeu IP? Há rota padrão? (`ip route`)
3. O gateway responde? (`ping` com cuidado; ping bloqueado não prova falha sozinho)
4. DNS resolve nome? Compare acesso por IP e por nome.
5. Algum firewall, VPN ou proxy mudou o caminho?

## Comandos úteis

~~~bash
ip addr
ip route
ping -c 4 exemplo.com
ss -tulpn
curl -I https://exemplo.com
wget --spider https://exemplo.com
~~~

- `ip addr`: interfaces/endereço.
- `ip route`: rotas/gateway.
- `ping -c 4`: envia quatro testes; não deixe ping infinito rodando sem necessidade.
- `ss -tulpn`: mostra sockets/portas; pode requerer privilégios para todos os detalhes.
- `curl -I`/`wget --spider`: testa resposta HTTP sem baixar conteúdo completo.

## NetworkManager

Em muitos desktops, NetworkManager gerencia Wi‑Fi, VPN e conexões. A interface gráfica é suficiente para uso normal; `nmcli` é a ferramenta de terminal associada em muitas distribuições.

Não copie comandos de rede com `sudo` que alteram rota, DNS ou firewall em sistema remoto sem acesso local/console de recuperação.

## SSH

SSH permite terminal remoto seguro. Use somente máquinas próprias ou autorizadas. Prefira chaves, senhas fortes, atualizações e firewall. Nunca exponha SSH à internet sem compreender usuários, chaves, logs e política de acesso.

## Exercício 🟡

Rode `ip addr` e `ip route`. Identifique a interface conectada, seu IP local e o gateway. Não publique esses dados em local público.
