# Cheat sheet — Permissões

| Letra | Valor | Significado |
| --- | --- | --- |
| `r` | 4 | leitura |
| `w` | 2 | escrita |
| `x` | 1 | execução/atravessar diretório |

| Ação | Exemplo | Observação |
| --- | --- | --- |
| Ver permissões | `ls -l arquivo` | Mostra dono, grupo e modo |
| Tornar script executável para dono | `chmod u+x script.sh` | Teste em arquivo próprio |
| Definir 640 | `chmod 640 arquivo` | Dono lê/escreve; grupo lê; outros não acessam |
| Mudar dono/grupo | `sudo chown usuario:grupo arquivo` | ⚠️ Não use recursivamente em sistema sem entender |

Evite `chmod -R 777`: abre acesso excessivo e frequentemente mascara problema de dono/grupo.
