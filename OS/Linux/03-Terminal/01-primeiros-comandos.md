# Terminal — primeiros comandos

## `pwd` — onde estou?

~~~bash
pwd
~~~

Mostra o caminho da pasta atual. Use sempre que estiver em dúvida antes de criar, mover ou apagar arquivos.

## `ls` — listar conteúdo

~~~bash
ls
ls -l
ls -la
~~~

- `-l`: detalhes como permissões, dono e data.
- `-a`: inclui arquivos ocultos.

Erro comum: achar que arquivo não existe porque ele começa com ponto; use `ls -la` para ver.

## `cd` — entrar em pasta

~~~bash
cd Documentos
cd ..
cd ~
cd /
~~~

- `cd ..` sobe uma pasta.
- `cd ~` volta para a pasta pessoal.
- `cd /` vai para raiz. Não significa que você deve modificar a raiz.

## `mkdir` — criar diretório

~~~bash
mkdir teste
mkdir -p projetos/exemplo/logs
~~~

`-p` cria pastas intermediárias se não existirem. Verifique com `pwd` e `ls` antes de criar estrutura grande.

## `touch` — criar arquivo vazio/atualizar data

~~~bash
touch anotacoes.txt
~~~

Ele não abre editor nem coloca conteúdo. Para escrever, use editor gráfico, `nano`, `vim` (se souber) ou redirecionamento com muito cuidado.

## `clear` e histórico

`clear` limpa a tela visualmente, mas não apaga histórico. Use setas ↑/↓ para rever comandos; não deixe senhas em comandos/histórico.

## Exercício 🟢

~~~bash
mkdir -p ~/linux-pratica/terminal
cd ~/linux-pratica/terminal
pwd
touch um.txt dois.txt tres.txt
ls -la
~~~

Confirme que você está na pasta correta e que os três arquivos apareceram.
