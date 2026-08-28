# 21 — RAG e bases de conhecimento

## O problema que RAG resolve

Um modelo não conhece automaticamente documentos internos, manuais novos ou regras específicas da sua empresa. RAG adiciona trechos relevantes de uma base de conhecimento ao contexto da pergunta antes de gerar a resposta.

## Fluxo simplificado

1. Coletar documentos autorizados.
2. Limpar e dividir em trechos com metadados.
3. Criar embeddings dos trechos.
4. Buscar os trechos mais relevantes para a pergunta.
5. Opcionalmente reordenar/reranquear resultados.
6. Entregar somente esses trechos ao modelo.
7. Responder com citações, limites e links para a origem.

## Componentes

| Termo | Papel |
| --- | --- |
| Chunk | Trecho menor de documento |
| Metadata | Fonte, data, seção, permissão e versão |
| Embedding | Vetor que representa significado |
| Banco vetorial | Armazena e busca embeddings |
| Retrieval | Recuperação de trechos relevantes |
| Reranking | Reordenação com critério mais preciso |
| Grounding | Resposta ancorada no material recuperado |

## RAG x fine-tuning

| RAG | Fine-tuning |
| --- | --- |
| Injeta informação atual no contexto | Ajusta comportamento de um modelo |
| Bom para documentos que mudam | Útil para tarefa/estilo repetitivo |
| Permite citar fonte | Não substitui uma base de fatos atualizada |
| Exige busca de qualidade | Exige dados de treinamento de qualidade |

Muitos projetos começam por RAG antes de considerar fine-tuning.

## Qualidade da base

- Remova versões antigas e duplicadas.
- Preserve título, data, origem e permissões.
- Divida por seções com sentido, não por tamanho cego.
- Teste perguntas reais e perguntas sem resposta.
- Faça o sistema dizer “não encontrei base suficiente” quando necessário.

## Prompt ancorado

> Responda somente com base nos trechos recuperados. Cite a fonte e a seção em cada afirmação relevante. Se os trechos não responderem, diga claramente que não há evidência suficiente. Não complete com conhecimento geral sem marcar isso.

## Avaliação

Crie conjunto de perguntas com resposta esperada, fonte correta e casos em que o sistema deve recusar. Meça se recuperou o trecho certo, se a resposta é fiel e se citou adequadamente.

Segurança importa: a base só deve fornecer documentos aos quais a pessoa tem acesso. Veja [Segurança e privacidade](./18-seguranca-e-privacidade.md).
