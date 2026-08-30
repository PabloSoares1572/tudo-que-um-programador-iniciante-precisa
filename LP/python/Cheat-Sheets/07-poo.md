# POO

\`\`\`python
from dataclasses import dataclass

@dataclass
class Produto:
    nome: str
    preco: float

    def com_desconto(self, percentual: float) -> float:
        return self.preco * (1 - percentual / 100)
\`\`\`

- classe = modelo; instância = objeto.
- \`self\` é a instância.
- prefira composição quando objeto “tem um” outro objeto.
- use \`dataclass\` para dados; não esqueça regras/validação.

