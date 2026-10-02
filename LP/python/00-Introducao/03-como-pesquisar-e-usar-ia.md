# Como pesquisar e usar IA para aprender

## Pesquise a causa, não só a solução

Uma boa busca contém: mensagem exata do erro, linguagem, versão quando relevante e contexto. Exemplo:

```text
Python TypeError unsupported operand type str int input
```

Leia primeiro a exceção e a linha apontada pelo traceback. Depois consulte a documentação oficial ou fontes da ferramenta envolvida.

## Uso saudável de IA

IA pode ajudar a explicar, revisar, gerar casos de teste ou sugerir pistas. Use pedidos como:

- “Explique esta mensagem de erro sem dar a solução completa.”
- “Dê três testes para esta função e explique o que cada um verifica.”
- “Revise este código procurando entrada inválida, mas preserve meu estilo.”
- “Compare minha solução com uma alternativa mais legível.”

## O que não fazer

- copiar um projeto inteiro sem entender;
- enviar chaves, senhas, dados de clientes ou código confidencial;
- aceitar comandos que apagam arquivos, instalam dependências ou acessam rede sem entender;
- presumir que uma resposta é atual só porque parece confiante.

## Método de verificação

1. Leia o código gerado linha a linha.
2. Execute em ambiente de teste.
3. Crie casos de borda: valor vazio, zero, valor grande e tipo errado.
4. Confira a API usada na documentação oficial.
5. Só então incorpore ao seu projeto.

O objetivo é se tornar independente; uma ferramenta deve acelerar seu aprendizado, não esconder a falta dele.

← [Python e versões](./02-python-origem-e-versoes.md) | [Preparar ambiente →](../01-Preparando-o-Ambiente/README.md)
