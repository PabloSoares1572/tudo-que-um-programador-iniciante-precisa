# Exercícios — base

## 🟢 1. Apresentação

**Objetivo:** praticar variável e f-string.

**Requisitos:** peça nome e cidade; mostre uma frase de apresentação.

**Dica:** \`input()\` devolve texto.

## 🟢 2. Próximo aniversário

**Objetivo:** converter entrada e fazer conta.

**Requisitos:** peça idade inteira e mostre a idade no próximo ano.

**Dica:** use \`int()\`.

## 🟡 3. Média de três notas

**Objetivo:** usar \`float\` e formatação.

**Requisitos:** calcule a média e mostre duas casas decimais.

**Dica:** \`f"{media:.2f}"\`.

## 🟡 4. Conversor de temperatura

**Objetivo:** aplicar fórmula e nomear variáveis.

**Requisitos:** converta Celsius para Fahrenheit usando \`F = C * 9 / 5 + 32\`.

---

## Soluções de referência — veja depois de tentar

### 1

\`\`\`python
nome = input("Nome: ")
cidade = input("Cidade: ")
print(f"{nome} mora em {cidade}.")
\`\`\`

### 2

\`\`\`python
idade = int(input("Idade: "))
print(f"No próximo ano você terá {idade + 1} anos.")
\`\`\`

### 3

\`\`\`python
notas = [float(input(f"Nota {indice}: ")) for indice in range(1, 4)]
media = sum(notas) / len(notas)
print(f"Média: {media:.2f}")
\`\`\`

A comprehension é opcional; uma versão com três variáveis também é válida no começo.

### 4

\`\`\`python
celsius = float(input("Temperatura em Celsius: "))
fahrenheit = celsius * 9 / 5 + 32
print(f"{celsius:.1f} °C = {fahrenheit:.1f} °F")
\`\`\`

← [Exercícios](./README.md) | [Controle de fluxo →](./02-controle-de-fluxo.md)

