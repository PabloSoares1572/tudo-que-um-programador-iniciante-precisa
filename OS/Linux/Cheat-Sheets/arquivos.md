# Cheat sheet — Arquivos e diretórios

| Ação | Forma segura | Cuidado |
| --- | --- | --- |
| Copiar arquivo | `cp -i origem destino` | `-i` pergunta antes de sobrescrever |
| Copiar pasta | `cp -r origem destino` | Confira origem/destino antes |
| Mover/renomear | `mv -i origem destino` | Pode sobrescrever sem `-i` |
| Remover arquivo | `rm -i arquivo` | Não é lixeira em geral |
| Encontrar arquivo | `find ~/pasta -type f -name "*.txt"` | Comece em pasta específica |
| Ver uso de disco | `df -h` | Mostra sistemas montados |
| Ver discos | `lsblk -f` | Leitura; identifique modelo/tamanho |

Use aspas para nomes com espaço: `cp "meu arquivo" "copia"`.
