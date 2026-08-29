# 04 — Usuários e permissões

## Modelo simples

Cada arquivo tem dono, grupo e permissões para três conjuntos: usuário dono, grupo e outros. As permissões básicas são:

- `r` (read): ler;
- `w` (write): escrever/alterar;
- `x` (execute): executar arquivo ou atravessar diretório.

Exemplo de `ls -l`:

~~~text
-rwxr-x--- 1 ana devs 1200 arquivo.sh
~~~

Os três blocos depois do tipo representam dono (`rwx`), grupo (`r-x`) e outros (`---`).

## Root e sudo

Root é a conta administrativa máxima. `sudo` concede ação administrativa conforme regras configuradas. Use-o para instalar/administrar, não para trabalhar em documentos comuns.

## `chmod`

### Simbólico

~~~bash
chmod u+x script.sh
chmod g-w arquivo.txt
~~~

`u` é dono, `g` é grupo, `o` são outros. Teste em arquivos seus.

### Numérico

Cada permissão vale: `r=4`, `w=2`, `x=1`. Então `640` significa dono `rw-` (6), grupo `r--` (4), outros `---` (0).

~~~bash
chmod 640 arquivo-confidencial.txt
~~~

Não existe número “bom para tudo”. Para diretórios, `x` tem efeito importante de acesso/atravessamento.

## `chown` e `chgrp`

~~~bash
sudo chown ana:devs arquivo.txt
sudo chgrp devs arquivo.txt
~~~

> ⚠️ Alterar dono/grupo de arquivos do sistema pode quebrar serviços. Não aplique recursivamente em `/`, `/usr`, `/etc` ou na pasta pessoal sem entender.

## Umask e ACL 🟡

- **umask:** influência nas permissões padrão de arquivos/diretórios novos.
- **ACL:** regras extras de acesso além de dono/grupo/outros.

Aprenda permissões básicas primeiro. Em ambiente profissional, consulte política de acesso e use grupos em vez de dar `sudo` a todos.

## Exercício 🟡

Na pasta de teste, crie arquivo `segredo.txt`, veja `ls -l`, retire permissão de leitura para outros e confirme com `ls -l`. Não use `sudo`.
