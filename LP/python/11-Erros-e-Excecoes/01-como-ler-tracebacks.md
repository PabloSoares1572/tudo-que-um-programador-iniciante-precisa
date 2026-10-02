# Como ler um traceback

Leia o traceback de baixo para cima:

1. a última linha mostra o tipo e a mensagem da exceção;
2. linhas anteriores mostram o caminho de chamadas até o problema;
3. localize o seu arquivo e a linha indicada;
4. observe os valores e tipos envolvidos;
5. reproduza com o menor exemplo possível.

Exemplo de mensagem:

```text
ValueError: invalid literal for int() with base 10: 'dez'
```

Ela informa que `int()` recebeu a string `"dez"`, que não representa um inteiro decimal. A correção pode ser pedir nova entrada, validar antes ou esclarecer a regra; não é simplesmente colocar `try/except` e ignorar o valor.

## Perguntas úteis

- Que valor chegou aqui?
- Qual tipo eu esperava e qual recebi?
- Qual chamada trouxe esse valor?
- Qual teste reproduz o problema?

← [Erros e exceções](./README.md) | [Estratégias →](./02-estrategias-de-tratamento.md)
