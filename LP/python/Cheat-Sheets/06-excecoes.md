# Exceções

\`\`\`python
try:
    numero = int(texto)
except ValueError:
    print("Número inválido")
else:
    print(numero)
finally:
    print("Sempre executa")

raise ValueError("Regra inválida")
\`\`\`

- Capture erro específico.
- Leia traceback de baixo para cima.
- Não use \`except: pass\`.
- Exceção esperada ≠ regra normal: valide quando for apropriado.

