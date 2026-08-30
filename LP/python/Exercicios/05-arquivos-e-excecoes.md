# Exercícios — arquivos e exceções

## 🟡 1. Diário seguro

**Requisitos:** grave uma anotação em \`dados_teste/diario.txt\` usando UTF-8 e \`with\`. Antes, crie a pasta com \`Path.mkdir\`.

## 🟡 2. Leitor de números

**Requisitos:** leia linhas de um arquivo, converta somente inteiros válidos e informe quantas foram ignoradas.

## 🔴 3. Configuração JSON

**Requisitos:** leia JSON de configuração, valide que possui \`nome\` (string) e \`ativo\` (booleano); apresente erro claro se o arquivo estiver ausente ou malformado.

## 🔴 4. CSV de notas

**Requisitos:** leia CSV com \`nome,nota\`, valide as notas e gere outro CSV apenas com alunos aprovados.

---

## Estratégia antes da solução

Liste as exceções que você espera: \`FileNotFoundError\`, \`JSONDecodeError\`, \`ValueError\` ou \`csv.Error\`. Não use um \`except\` genérico para tudo.

## Solução de referência (recorte do exercício 2)

\`\`\`python
from pathlib import Path

numeros = []
ignoradas = 0

for linha in Path("dados_teste/numeros.txt").read_text(encoding="utf-8").splitlines():
    try:
        numeros.append(int(linha))
    except ValueError:
        ignoradas += 1

print(f"Soma: {sum(numeros)}; ignoradas: {ignoradas}")
\`\`\`

Melhore a referência verificando se o arquivo existe, evitando carregar arquivo gigante inteiro e registrando qual linha era inválida.

← [Funções](./04-funcoes.md) | [POO e testes →](./06-poo-e-testes.md)

