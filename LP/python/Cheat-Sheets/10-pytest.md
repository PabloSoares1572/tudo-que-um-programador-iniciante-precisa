# pytest

\`\`\`python
def somar(a, b):
    return a + b

def test_somar():
    assert somar(2, 3) == 5
\`\`\`

\`\`\`text
python -m pytest
python -m pytest -q
\`\`\`

- Nome de teste começa com \`test_\`.
- Teste normal, limite e erro.
- Use fixture para preparo reutilizável.
- Mock isola dependência externa, não substitui teste de integração.

