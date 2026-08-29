# 02 — Sistema de arquivos Linux

## Explicação simples

No Linux, tudo começa em `/`, chamado de raiz. Discos, partições e dispositivos são conectados à árvore de diretórios em pontos de montagem; não existem letras de unidade como `C:` e `D:` no modelo tradicional do Windows.

## Diretórios importantes

| Caminho | Propósito | Cuidado |
| --- | --- | --- |
| `/` | Raiz de toda a árvore | Nunca apague/alterne conteúdo sem saber |
| `/home` | Pastas pessoais de usuários | Seus documentos normalmente ficam aqui |
| `/etc` | Configurações do sistema | Edite somente com backup e documentação |
| `/var` | Dados variáveis: logs, cache, filas | Pode crescer; investigue antes de apagar |
| `/usr` | Programas, bibliotecas e dados compartilhados | Gerenciado por pacotes em geral |
| `/tmp` | Arquivos temporários | Não use para dados importantes |
| `/boot` | Arquivos de boot/kernel | Alterações podem quebrar inicialização |
| `/dev` | Representações de dispositivos | `sda`, `nvme0n1` etc.; não escreva sem confirmar |
| `/proc` | Informações do kernel/processos em tempo real | Virtual, não é pasta comum |
| `/sys` | Informações/controles de dispositivos e kernel | Avançado; cuidado com escrita |
| `/media` e `/mnt` | Pontos comuns para unidades montadas | Varia por distribuição/configuração |

## Caminhos absolutos e relativos

- **Absoluto:** começa em `/`, exemplo `/home/ana/Documentos`.
- **Relativo:** parte da pasta atual, exemplo `Documentos` ou `../Fotos`.
- `.` significa pasta atual; `..` significa pasta pai.
- `~` representa a pasta pessoal do usuário atual.

## Montar e desmontar

“Montar” significa tornar conteúdo de uma partição acessível em um diretório. Pendrives normalmente são montados automaticamente pela interface gráfica. Em administração, você pode usar `mount`, `umount`, `findmnt` e `/etc/fstab` — veja [Discos e partições](./07-discos-e-particoes.md).

> ⚠️ Remover fisicamente uma unidade enquanto ela está sendo gravada pode corromper dados. Ejete/desmonte pela interface ou comando apropriado antes de remover.

## Permissões e arquivos ocultos

Arquivos que começam com `.` são ocultos por convenção e costumam guardar configurações, como `.config`. Não apague pastas ocultas por “limpeza” sem saber o que elas contêm.

## Exercício 🟢

No terminal, execute:

~~~bash
pwd
ls -la ~
ls /
~~~

Identifique sua pasta pessoal e três diretórios do sistema. Não edite nada ainda.
