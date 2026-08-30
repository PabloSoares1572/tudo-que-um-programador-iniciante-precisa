# 17 — Debugging: encontrar a causa

> 🟡 **Intermediário**

Debugging é um processo. A sequência recomendada é:

```text
Observar sintoma → reproduzir → reduzir o caso → formular hipótese
→ inspecionar valores → testar uma mudança → confirmar → criar teste contra regressão
```

## Ferramentas

- traceback para localizar a falha;
- `print` temporário e bem localizado;
- debugger com breakpoint e inspeção de variáveis;
- logs para aplicações e erros que não ocorrem no seu computador;
- testes para reproduzir e impedir retorno do bug.

## Breakpoints

Pausar antes da linha suspeita permite verificar valores, tipos e caminho executado. Use “step over” para avançar linha a linha e “step into” só quando realmente precisa entrar em outra função.

## Não faça

- alterar dez linhas e não saber o que resolveu;
- apagar o traceback antes de ler;
- esconder a exceção com `except Exception: return None`;
- testar diretamente em dados de produção.

## Próximo

- [Metodologia e logging](./01-metodologia-e-logging.md)

← [Testes](../16-Testes/README.md) | [Ambientes e dependências →](../18-Ambientes-e-Dependencias/README.md)
