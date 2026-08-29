# 09 — Segurança Linux

## Princípios

Linux não dispensa segurança. A defesa vem de atualizações, menor privilégio, serviços mínimos, autenticação forte, logs, backup e revisão de mudanças.

## Checklist de desktop

- Atualize pelo repositório oficial.
- Use senha forte e bloqueio de tela.
- Use conta normal; reserve `sudo` para tarefas administrativas.
- Instale software de fontes confiáveis.
- Remova extensões/repositórios não usados.
- Faça backup e teste a restauração.
- Desconfie de scripts que pedem `curl | sudo sh`.

## Checklist de servidor

- Aplique atualizações em janela planejada e monitore após reinício.
- Restrinja SSH a usuários/chaves autorizados; evite login root remoto.
- Exponha somente portas/serviços necessários.
- Configure firewall com regra mínima e acesso de recuperação.
- Revise `systemctl`, contas, grupos e logs regularmente.
- Faça backup criptografado e teste restauração.
- Registre mudanças e mantenha inventário de serviços.

## Permissões e menor privilégio

Dar `sudo` a todo usuário ou executar serviço como root amplia impacto de erro. Crie usuários/grupos específicos e conceda apenas acesso necessário. Consulte [Usuários e permissões](./04-usuarios-e-permissoes.md).

## Criptografia e chaves

Criptografia de disco protege dados em caso de perda física, mas aumenta importância de senha/chave de recuperação. Guarde informações de recuperação em local seguro, separado do computador. Nunca coloque chaves privadas em repositório público.

## Firewall e logs

Firewall controla tráfego, mas uma regra errada pode cortar seu próprio acesso. Antes de mudar firewall de servidor, tenha console/acesso alternativo e veja regras atuais. Logs ajudam a investigar — não apague logs para “limpar” antes de entender o problema.

## Segurança ofensiva

Pratique somente em laboratório ou sistemas com autorização explícita. Aprender defesa, análise de logs e hardening é permitido e útil; explorar terceiros sem permissão não é.
