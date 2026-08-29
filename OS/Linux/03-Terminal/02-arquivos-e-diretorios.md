# Terminal — arquivos e diretórios

## Copiar com `cp`

~~~bash
cp um.txt copia-um.txt
cp -i um.txt copia-um.txt
cp -r pasta-origem pasta-copia
~~~

- `-i` pergunta antes de sobrescrever.
- `-r` copia diretórios recursivamente. Use somente após conferir origem e destino.

## Mover/renomear com `mv`

~~~bash
mv dois.txt renomeado.txt
mv -i renomeado.txt ../
~~~

O mesmo comando move ou renomeia. Com destino existente, ele pode sobrescrever; durante aprendizado, prefira `-i`.

## Remover com `rm`

~~~bash
rm -i copia-um.txt
~~~

> ⚠️ `rm` remove arquivos; em geral não envia para lixeira. Use `rm -i` para uma confirmação extra e confira `pwd` + `ls` antes.

Para remover diretório vazio, existe `rmdir pasta-vazia`. Para diretórios com conteúdo, existem opções recursivas perigosas — elas não são um exercício iniciante. Se precisar limpar um diretório, primeiro faça backup e remova arquivos específicos com confirmação.

## Ler conteúdo sem editar

~~~bash
cat um.txt
less arquivo-grande.log
head -n 20 arquivo.txt
tail -n 20 arquivo.txt
tail -f arquivo.log
~~~

- `cat`: bom para conteúdo curto.
- `less`: permite navegar; pressione `q` para sair.
- `head`/`tail`: mostram começo/fim.
- `tail -f`: acompanha linhas novas em log; encerre com `Ctrl+C`.

## Nomes com espaço

Use aspas:

~~~bash
cp "meu arquivo.txt" "copia segura.txt"
~~~

Evite nomes com espaço em scripts; use hífen ou sublinhado quando possível.

## Exercício 🟢

1. Copie `um.txt` para `copia-um.txt` usando `-i`.
2. Renomeie `tres.txt` para `terceiro.txt`.
3. Abra a pasta com `ls -la`.
4. Remova apenas a cópia usando `rm -i` depois de confirmar o nome.
