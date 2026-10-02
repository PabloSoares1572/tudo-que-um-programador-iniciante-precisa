# Princípios e design patterns com moderação

## Princípios

| Princípio | Uso saudável |
| --- | --- |
| DRY | reduza duplicação de conhecimento, não toda repetição visual |
| KISS | prefira solução simples que atende o problema |
| YAGNI | não construa extensão hipotética sem necessidade |
| SOLID | heurísticas para coesão, abstração e dependências; não uma lista de classes |
| Separation of concerns | separe responsabilidades que mudam por motivos diferentes |

## Patterns

Factory, Strategy, Observer, Adapter e Repository podem ser úteis quando há variação real, integração ou dependência substituível. Primeiro escreva a solução direta e identifique a dor. Um pattern aplicado cedo pode esconder regra simples atrás de várias classes.

## Dependency injection

Passar dependências como argumento ou construtor facilita testes e troca de implementação. Não é necessário um framework de injeção para começar.

← [Boas práticas](./README.md) | [Documentação →](./02-documentacao-e-revisao.md)

