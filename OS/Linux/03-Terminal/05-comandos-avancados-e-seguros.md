# Terminal — comandos avançados e segurança

## Ajuda antes de ação

~~~bash
man ls
ls --help
type cd
which python
~~~

- `man`: manual instalado.
- `--help`: resumo de opções.
- `type`: informa se algo é comando interno, alias ou executável.
- `which`: pode localizar executável, mas não é fonte definitiva de configuração.

## `sudo`

`sudo comando` pede autorização administrativa para um comando específico. Ele registra e amplia o impacto da ação; não use para evitar mensagem de permissão sem entender a causa.

## Comandos de alto risco

| Categoria | Exemplos | Risco | Alternativa inicial |
| --- | --- | --- |
| Remoção recursiva | `rm` com opções recursivas | Apagar muitos arquivos sem lixeira | Listar com `find`, mover cópia, usar `rm -i` em item específico |
| Escrita em disco | `dd`, `mkfs`, ferramentas de partição | Destruir partições/arquivos | `lsblk -f`, backup, Live USB e guia específico |
| Permissões em massa | `chmod -R`, `chown -R` | Quebrar acesso/segurança | Aplicar a um arquivo/pasta de teste |
| Sistema de boot | GRUB, EFI, initramfs | PC pode não iniciar | Backup, documentação da distribuição, procedimento de recuperação |
| Firewall/serviços | `systemctl`, regras de firewall | Perder acesso ou expor serviço | Conferir status/regras e testar localmente |

## Método seguro de comando

1. Leia o comando e cada argumento.
2. Descubra que usuário e pasta/disco serão afetados.
3. Rode versão de diagnóstico/listagem quando existir.
4. Faça backup/snapshot se a ação for modificadora.
5. Execute em escopo mínimo.
6. Confirme resultado e registre como reverter.

## Exercício 🔴

Escolha um comando administrativo **somente para estudar**. Leia `man`, explique seu efeito com suas palavras e proponha um laboratório em VM. Não execute em sistema principal até saber verificar e desfazer.
