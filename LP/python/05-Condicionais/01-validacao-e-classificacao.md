# Validação e classificação sem confusão

## Valide antes de processar

Se uma regra só aceita idade entre 0 e 130, verifique isso antes de classificar. Uma validação não é “detalhe”: ela impede resultados sem sentido.

```python
idade = int(input("Idade: "))

if not 0 <= idade <= 130:
    print("Idade inválida")
elif idade >= 60:
    print("Grupo: idoso")
elif idade >= 18:
    print("Grupo: adulto")
else:
    print("Grupo: menor de idade")
```

## Ordem das condições importa

Python para no primeiro bloco verdadeiro de uma cadeia `if`/`elif`/`else`. Se você testar `idade >= 18` antes de `idade >= 60`, uma pessoa de 70 será classificada como adulta e nunca chegará à regra de idoso. Teste do mais específico ao mais geral quando os intervalos se sobrepõem.

## `match` como recurso posterior

Python moderno possui `match` para comparar padrões. Ele é útil em casos específicos, mas não precisa substituir `if` no início. Domine condições booleanas antes de adotá-lo.

## Exercício

Classifique uma compra em frete grátis, frete reduzido ou frete normal baseado no valor. Escreva cinco casos de teste em comentário antes de programar.

← [Condicionais](./README.md) | [Loops →](../06-Loops/README.md)
