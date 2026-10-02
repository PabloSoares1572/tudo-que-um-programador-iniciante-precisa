# Metodologia de debugging e logging

## Diagnóstico por hipótese

Em vez de “tentar coisas”, formule uma hipótese verificável: “a entrada chega como string, mas a função espera inteiro”. Adicione uma observação mínima, reproduza e confirme/refute. Isso cria aprendizado reutilizável.

## Logging

Logs registram eventos para entender uma aplicação sem pausar sua execução. Use níveis:

- `DEBUG`: detalhe de desenvolvimento;
- `INFO`: eventos esperados importantes;
- `WARNING`: algo inesperado, mas aplicação segue;
- `ERROR`: operação falhou;
- `CRITICAL`: falha grave.

```python
import logging

logging.basicConfig(level=logging.INFO)
logging.info("Aplicação iniciada")
```

Nunca grave senha, token, cartão, chave de API ou dado pessoal sensível em logs. Use mensagens que expliquem contexto sem expor segredo.

## Depois da correção

Documente a causa curta, crie um teste quando possível e remova `print`s de diagnóstico que não têm propósito permanente.

← [Debugging](./README.md) | [Ambientes →](../18-Ambientes-e-Dependencias/README.md)
