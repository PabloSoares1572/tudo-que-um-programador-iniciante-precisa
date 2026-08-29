# 06 — Processos e serviços

## Processo, PID e job

Um **processo** é programa em execução. Cada processo recebe um **PID**. Um **job** é uma tarefa associada ao shell atual, que pode estar em primeiro plano ou segundo plano.

## Observar antes de encerrar

~~~bash
ps aux
top
htop
pgrep -a nome
~~~

- `ps aux`: lista processos em um instante.
- `top`: visão dinâmica; pressione `q` para sair.
- `htop`: interface mais amigável, se instalada.
- `pgrep -a`: procura processo e mostra comando associado.

Não encerre processo só porque usa CPU/memória. Ele pode ser atualização, backup, indexação ou serviço importante.

## Sinais e `kill`

~~~bash
kill PID
kill -TERM PID
~~~

O `kill` envia sinal; o padrão costuma pedir término educado (`TERM`). Sinais forçados existem, mas devem ser última opção, depois de identificar o processo e tentar fechamento normal.

> ⚠️ Encerrar processo errado pode perder trabalho, corromper dados ou derrubar sessão. Nunca use comandos de término amplo por nome sem confirmar o que corresponde.

## systemd e serviços

Muitas distribuições usam systemd para iniciar e gerenciar serviços.

~~~bash
systemctl status nome-do-servico
sudo systemctl start nome-do-servico
sudo systemctl stop nome-do-servico
sudo systemctl restart nome-do-servico
sudo systemctl enable nome-do-servico
~~~

- `status` é diagnóstico e não altera nada.
- `start`/`stop` controlam agora.
- `enable` configura início futuro; não é o mesmo que iniciar agora.

Não desative serviços “para otimizar” sem descobrir dependências e finalidade.

## Logs com `journalctl`

~~~bash
journalctl -b
journalctl -b -p err
journalctl -u nome-do-servico
~~~

- `-b`: boot atual.
- `-p err`: mensagens de severidade erro.
- `-u`: filtra serviço.

Ao pedir ajuda, copie mensagem relevante e contexto, não apenas “deu erro”. Remova dados sensíveis de logs.

## Exercício 🟡

Encontre um serviço conhecido do seu sistema com `systemctl status` e leia o estado. Não inicie, pare ou habilite serviços aleatórios.
