# 10 — Shell e scripts

> 🟡 Aprenda automação em pasta de teste ou VM. Um script pode repetir um erro centenas de vezes rapidamente.

## Primeiro script

~~~bash
#!/usr/bin/env bash
set -euo pipefail

nome="mundo"
printf 'Olá, %s!\n' "$nome"
~~~

- **Shebang:** escolhe interpretador.
- `set -euo pipefail`: ajuda a não ignorar certos erros/variáveis; compreenda seus efeitos antes de usar em todo contexto.
- Aspas em `"$variavel"` evitam divisão inesperada de palavras em vários casos.

## Conceitos a dominar

| Tema | Para que serve |
| --- | --- |
| Variáveis | Guardar valores |
| Argumentos | Receber dados como `$1`, `$2` |
| Condições | Escolher caminho com `if`/`case` |
| Loops | Repetir com `for`/`while` |
| Funções | Reutilizar blocos |
| Exit code | Indicar sucesso (`0`) ou falha (outro valor) |
| Pipes | Passar saída a outro comando |
| Redirecionamento | Gravar/ler dados com cuidado |
| `grep`, `sed`, `awk` | Filtrar e transformar texto |
| Cron/systemd timers | Agendar tarefas conforme distribuição/uso |

## Script seguro de exemplo

~~~bash
#!/usr/bin/env bash
set -euo pipefail

origem="${1:-}"
destino="${2:-}"

if [[ -z "$origem" || -z "$destino" ]]; then
  printf 'Uso: %s ORIGEM DESTINO\n' "$0" >&2
  exit 2
fi

if [[ ! -d "$origem" ]]; then
  printf 'Origem não é diretório: %s\n' "$origem" >&2
  exit 1
fi

printf 'Origem: %s\nDestino: %s\n' "$origem" "$destino"
printf 'Modo demonstração: nenhum arquivo foi copiado.\n'
~~~

Ele valida entradas e faz uma prévia sem escrever. Em automação real, acrescente logs, testes e confirmação antes de ações destrutivas.

## `sed` e `awk`

São poderosos para texto. Use arquivo de cópia e produza saída em arquivo novo até entender expressão. Não aplique substituições globais em configurações de produção sem backup e teste.

## Agendamento

Cron é tradicional; systemd timers são comuns em sistemas com systemd. Agendar um comando é fácil; garantir que ele seja idempotente, tenha logs, lide com falhas e não exponha segredos é a parte profissional.

## Exercícios

1. Crie script que receba um nome e imprima saudação.
2. Faça ele retornar código não zero se argumento estiver vazio.
3. Acrescente `--dry-run` que só mostra o que faria.
4. Execute em pasta de teste e leia o código antes de torná-lo executável.
