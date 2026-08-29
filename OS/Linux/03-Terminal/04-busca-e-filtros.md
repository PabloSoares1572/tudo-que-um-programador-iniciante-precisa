# Terminal — busca e filtros

## `grep` — localizar texto

~~~bash
grep "erro" arquivo.log
grep -i "erro" arquivo.log
grep -n "erro" arquivo.log
~~~

- `-i`: ignora maiúsculas/minúsculas.
- `-n`: mostra número da linha.

Use aspas em padrões simples. Expressões regulares são poderosas, mas precisam de estudo; teste em cópias.

## `find` — localizar arquivos

~~~bash
find ~/linux-pratica -type f -name "*.txt"
find ~/linux-pratica -type d -name "teste"
~~~

Comece sempre em uma pasta específica. Procurar a partir de `/` pode ser lento e gerar mensagens de permissão.

## `wc`, `sort`, `uniq`

~~~bash
wc -l arquivo.txt
sort nomes.txt | uniq
sort nomes.txt | uniq -c
~~~

- `wc -l`: conta linhas.
- `sort`: ordena.
- `uniq`: remove repetições **adjacentes**; por isso costuma vir depois de `sort`.

## `cut` e `awk`

`cut` separa campos simples por delimitador. `awk` é uma linguagem de processamento de texto mais poderosa; comece com pequenos arquivos CSV de teste e valide o resultado antes de usar em dados reais.

~~~bash
cut -d ',' -f 1 exemplo.csv
awk -F ',' '{print $1}' exemplo.csv
~~~

Não execute filtros que sobrescrevem o mesmo arquivo de entrada sem backup: muitas ferramentas truncam o arquivo antes de terminarem de ler.

## Exercício 🟡

1. Crie arquivo de teste com nomes repetidos.
2. Conte linhas com `wc -l`.
3. Ordene e remova repetições, enviando resultado para **outro arquivo**.
4. Compare os dois arquivos com `cat` ou `diff` se disponível.
