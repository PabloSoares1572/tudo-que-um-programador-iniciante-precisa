# Exercícios — condicionais e loops

## 🟢 1. Par ou ímpar

**Requisitos:** peça um inteiro e informe se é par ou ímpar.

**Dica:** o resto de divisão por 2 é \`numero % 2\`.

## 🟡 2. Situação escolar

**Requisitos:** valide nota entre 0 e 10 e classifique em aprovado (≥ 7), recuperação (≥ 5) ou reprovado.

## 🟡 3. Tabuada

**Requisitos:** mostre a tabuada de 1 a 10 do número informado usando \`for\`.

## 🔴 4. Senha com tentativas

**Requisitos:** permita no máximo três tentativas para uma senha fictícia; encerre cedo em caso de acerto.

**Dica:** use \`break\` apenas quando acertar.

---

## Soluções de referência

### 1

\`\`\`python
numero = int(input("Número inteiro: "))
if numero % 2 == 0:
    print("Par")
else:
    print("Ímpar")
\`\`\`

### 2

\`\`\`python
nota = float(input("Nota: "))
if not 0 <= nota <= 10:
    print("Nota inválida")
elif nota >= 7:
    print("Aprovado")
elif nota >= 5:
    print("Recuperação")
else:
    print("Reprovado")
\`\`\`

### 3

\`\`\`python
numero = int(input("Número: "))
for multiplicador in range(1, 11):
    print(f"{numero} x {multiplicador} = {numero * multiplicador}")
\`\`\`

### 4

\`\`\`python
senha_correta = "python123"

for tentativa in range(1, 4):
    senha = input(f"Tentativa {tentativa}/3: ")
    if senha == senha_correta:
        print("Acesso liberado")
        break
else:
    print("Tentativas esgotadas")
\`\`\`

Nunca use senha hardcoded em aplicação real; o exercício ensina fluxo, não autenticação segura.

← [Base](./01-base.md) | [Coleções →](./03-colecoes.md)

