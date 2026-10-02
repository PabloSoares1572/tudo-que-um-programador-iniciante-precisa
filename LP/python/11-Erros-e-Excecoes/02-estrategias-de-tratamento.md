# Estratégias de tratamento de exceções

## Quando tratar

Trate uma exceção quando você tem uma ação útil: pedir novo dado, usar valor alternativo documentado, registrar o problema ou liberar um recurso.

## Quando deixar aparecer

Durante desenvolvimento, uma exceção inesperada deve aparecer com traceback para ser corrigida. Capturar `Exception` no topo só é aceitável se você registrar detalhes e apresentar mensagem adequada sem esconder a causa.

## Exceção não é condição normal

Use `if` para regras esperadas, como campo vazio; use exceções para falhas excepcionais, como erro de arquivo ou conversão que não deveria ocorrer depois de validação. A fronteira depende do contexto, mas não use exceptions como fluxo principal sem motivo.

## Criando exceções próprias

Em projetos maiores, exceções específicas podem comunicar domínio com clareza. Só crie classes próprias quando o tratamento realmente precisar distinguir aquela categoria.

← [Tracebacks](./01-como-ler-tracebacks.md) | [POO →](../12-POO/README.md)
