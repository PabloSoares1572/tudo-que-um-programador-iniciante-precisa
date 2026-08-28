# 01 — Fundamentos de Inteligência Artificial

## O que é IA?

Inteligência Artificial é o nome dado a sistemas capazes de executar tarefas que normalmente exigiriam parte da inteligência humana: reconhecer padrões, classificar informações, gerar texto, tomar decisões sob regras ou sugerir opções.

IA não é uma única tecnologia. Um filtro de spam, uma recomendação de filme e um assistente que conversa são usos diferentes de IA.

## Mapa rápido dos conceitos

| Termo | Explicação simples | Exemplo |
| --- | --- | --- |
| Machine Learning | Sistema aprende padrões a partir de dados | Identificar e-mails suspeitos |
| Deep Learning | Machine Learning com redes neurais maiores | Reconhecer objetos em imagens |
| Rede neural | Modelo inspirado de forma simplificada em conexões neurais | Encontrar relações complexas em dados |
| IA generativa | IA que cria conteúdo novo | Gerar um resumo ou uma imagem |
| LLM | Modelo de linguagem grande, focado em texto | Assistente que responde perguntas |
| Multimodal | Trabalha com mais de um tipo de mídia | Ler imagem e responder em texto |

## Como uma IA generativa parece “saber” coisas?

Ela aprendeu relações estatísticas em muitos exemplos durante o treinamento. Quando recebe um pedido, calcula qual continuação tem mais chance de ser útil segundo seus padrões e instruções.

Isso é diferente de possuir memória perfeita, opinião própria ou garantia de verdade. Uma resposta fluente pode estar errada.

## Tokens e janela de contexto

- **Token:** pedaço de texto que o modelo processa. Uma palavra pode virar um ou mais tokens.
- **Janela de contexto:** quantidade máxima de informação que o modelo consegue considerar de uma vez na conversa ou arquivo.

Quando uma conversa ou documento ultrapassa o limite disponível, partes mais antigas podem deixar de ser consideradas, ser resumidas ou precisar ser reenviadas. Por isso, contexto relevante é mais importante que contexto enorme.

## Termos importantes sem mistério

### Transformers

É uma arquitetura de modelos muito usada em linguagem. Ela ajuda o modelo a relacionar partes de um texto entre si, por exemplo conectar “ele” à pessoa mencionada antes.

### Embeddings

São representações numéricas de significado. Textos parecidos tendem a ficar próximos nessa representação. Eles são úteis para busca semântica e RAG.

### Fine-tuning

É um novo treinamento especializado de um modelo já existente para determinado comportamento, tarefa ou estilo. Nem todo problema precisa de fine-tuning: muitas vezes um bom prompt, exemplos ou RAG resolvem primeiro.

### RAG

**Retrieval-Augmented Generation**: antes de responder, o sistema busca trechos relevantes em uma base de documentos e os entrega ao modelo como contexto. Veja [RAG e bases de conhecimento](./21-rag-e-bases-de-conhecimento.md).

### Agentes

Um agente combina modelo, objetivo, ferramentas e etapas de execução. Em vez de apenas responder, ele pode pesquisar, ler arquivos, criar tarefas ou propor alterações — sempre dentro das permissões recebidas.

## Tipos de modelo

| Tipo | Entrada e saída comuns | Uso típico |
| --- | --- | --- |
| Texto | Texto → texto | Conversa, resumo, código |
| Imagem | Texto/imagem → imagem | Ilustração e edição |
| Vídeo | Texto/imagem → vídeo | Protótipos e conteúdo audiovisual |
| Áudio | Texto/áudio → áudio | Transcrição, voz e música |
| Raciocínio | Problema → plano/solução | Tarefas estruturadas e análise |

Um mesmo produto pode combinar vários desses tipos.

## Exemplo simples

**Pedido:** “Resuma este texto em cinco tópicos para um aluno do ensino médio.”

O modelo não lê como uma pessoa. Ele transforma o texto em tokens, identifica padrões e produz uma sequência provável que respeite “cinco tópicos” e “ensino médio”. Se o texto tiver um erro, a IA pode preservá-lo; se o pedido for vago, ela pode escolher um foco diferente do desejado.

## Exercício

Pegue uma tarefa que você faria com IA e responda:

1. Qual é a entrada? Texto, imagem, dados ou arquivo?
2. Qual resultado você precisa receber?
3. Qual parte precisa ser verificada por você?
4. Um prompt basta ou você precisa de documentos, ferramentas ou revisão humana?

Próximo: [Como modelos generativos funcionam](./02-como-modelos-generativos-funcionam.md).
