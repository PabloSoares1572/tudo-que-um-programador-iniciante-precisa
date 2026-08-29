# Terminal — pipes e redirecionamento

> 🟡 Antes de usar `>` ou `>>`, confirme o arquivo de destino. Um redirecionamento pode sobrescrever conteúdo.

## Pipe `|`

Um pipe envia a saída de um comando para o próximo.

~~~bash
ls -la | less
ps aux | less
~~~

Isso não grava arquivo; apenas encadeia dados na tela.

## Redirecionamento de saída

~~~bash
comando > saida.txt
comando >> saida.txt
~~~

- `>` cria ou **sobrescreve** o arquivo.
- `>>` acrescenta no fim.

Forma segura para aprender:

~~~bash
pwd
ls -l saida.txt
printf 'teste\n' >> arquivo-de-teste.txt
cat arquivo-de-teste.txt
~~~

Nunca use `sudo comando > arquivo-do-sistema` achando que o `sudo` cobre o redirecionamento; o shell pode abrir o arquivo antes. Para configurações do sistema, use método documentado pela sua distribuição e faça backup.

## Entrada padrão e erros

- `stdin`: entrada padrão, geralmente teclado.
- `stdout`: saída normal, geralmente tela.
- `stderr`: mensagens de erro, geralmente tela.

Você verá referências a `2>` e `2>&1` em scripts; trate como tópico intermediário e teste em arquivos temporários, não em logs/sistema importante.

## `tee`

`tee` mostra saída e grava em arquivo. Exemplo seguro em pasta de teste:

~~~bash
printf 'linha de teste\n' | tee -a anotacoes.txt
~~~

`-a` acrescenta. Sem `-a`, ele sobrescreve o arquivo.

## Exercício 🟡

Crie um arquivo em `~/linux-pratica` com uma lista de seus arquivos, usando `>>` para acrescentar duas vezes. Abra com `cat` e confira que não escreveu em pasta do sistema.
