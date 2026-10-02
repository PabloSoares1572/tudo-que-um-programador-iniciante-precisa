# Shell, subprocess e automação segura

\`subprocess\` permite chamar programas externos, mas aumenta risco: uma string montada com entrada externa pode virar command injection. Sempre prefira APIs Python; se precisar chamar um programa conhecido, passe uma lista de argumentos fixa/validada e evite \`shell=True\`.

\`\`\`python
import subprocess

resultado = subprocess.run(
    ["python3", "--version"],
    check=True,
    capture_output=True,
    text=True,
)
print(resultado.stdout)
\`\`\`

O exemplo consulta a versão do interpretador e não usa entrada de usuário. Antes de automatizar ferramenta externa, confirme documentação, permissões, diretório de trabalho e comportamento em falha.

## Checklist

- argumentos permitidos são uma lista fechada?
- arquivos alvo estão dentro da pasta esperada?
- existe modo \`--dry-run\`/simulação?
- logs não expõem segredo?
- é possível interromper/reverter?

← [Automação](./README.md) | [Web →](../22-Web/README.md)

