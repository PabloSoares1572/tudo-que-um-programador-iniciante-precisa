# 20 — Agentes de IA

## O que é um agente?

Um agente é um sistema que combina um modelo com objetivo, contexto, etapas e ferramentas. Ele pode decidir uma próxima ação dentro de limites definidos: buscar um arquivo, consultar uma base, abrir uma tarefa ou propor uma alteração.

Um agente não deve receber liberdade ilimitada por padrão. Quanto maior o poder de agir, maior a necessidade de escopo, permissões, testes e supervisão.

## Componentes

| Componente | Função |
| --- | --- |
| Objetivo | Resultado que deve atingir |
| Instruções | Regras, prioridades e limites |
| Contexto | Dados e documentos relevantes |
| Memória | Informação persistida, quando disponível e permitida |
| Ferramentas | Pesquisa, arquivos, banco, calendário, código etc. |
| Planejamento | Divisão da tarefa em etapas |
| Execução | Chamadas de ferramenta e produção de saída |
| Avaliação | Testes, checklist, logs e aprovação |

## Chamada de ferramenta não é mágica

Uma ferramenta é uma ação concreta, com parâmetros e permissões. O agente pode sugerir “criar arquivo”, mas a ação só deve ocorrer se a ferramenta existe, os parâmetros são válidos e a permissão foi concedida.

## Níveis de autonomia

| Nível | Exemplo | Proteção |
| --- | --- | --- |
| Somente leitura | Resumir repositório | Escopo de arquivos e logs |
| Proposta | Gerar plano ou patch | Revisão humana antes de aplicar |
| Ação reversível | Criar branch, rascunho ou ticket | Prévia e rollback |
| Ação sensível | Enviar mensagem, mudar produção | Aprovação explícita e auditoria |

## Tarefa boa para um agente de código

~~~text
Antes de modificar:
1. analise a estrutura e tecnologias;
2. leia os arquivos relevantes;
3. descreva o plano e arquivos afetados;
4. implemente em branch separada;
5. rode testes, linter e build;
6. informe arquivos alterados, riscos e como validar;
7. não acesse segredos nem execute ações fora do escopo.
~~~

## Quando não usar agente

- a tarefa é menor que o tempo de configurar e revisar;
- os dados são sensíveis e não há ambiente autorizado;
- não existe teste ou critério de aceitação;
- a ação é irreversível e não há aprovação humana;
- o problema exige decisão especializada que não pode ser delegada.

Leia [IA em repositórios](./24-ia-em-repositorios.md), [Automações](./22-automacoes-com-ia.md) e [Segurança](./18-seguranca-e-privacidade.md).
