# 23 — APIs de IA

## O que é uma API de IA?

É uma interface para enviar dados a um modelo e receber uma resposta programaticamente. Assim, seu sistema pode resumir texto, classificar pedidos, extrair campos ou gerar conteúdo dentro de regras próprias.

## Conceitos essenciais

| Termo | Significado |
| --- | --- |
| Endpoint | Endereço da funcionalidade da API |
| Chave de API | Credencial para autenticar chamadas |
| Request | Dados enviados, como mensagens e parâmetros |
| Response | Resultado devolvido pela API |
| Token | Unidade usada no processamento e, em geral, no custo |
| Rate limit | Limite de chamadas por período |
| Webhook | Evento enviado por um serviço a outro |

## Nunca exponha uma chave

Não coloque API keys em frontend público, repositório, print ou prompt. Use variáveis de ambiente e cofres de segredo apropriados. Revogue e troque chaves expostas imediatamente conforme as regras do provedor.

## Fluxo de integração

1. Defina um caso de uso estreito.
2. Escolha modelo e formato de saída.
3. Valide entrada no seu backend.
4. Chame a API com timeout e tratamento de erro.
5. Valide a saída: JSON, tipos, campos e limites.
6. Registre métricas sem vazar conteúdo sensível.
7. Teste custo, latência, qualidade e casos de falha.

## Pseudocódigo seguro

~~~text
entrada = validarEntrada(request)
prompt = montarPrompt(entrada)
resposta = chamarModeloComTimeout(prompt)
dados = validarJSON(resposta)

se dados inválidos:
  retornar erro controlado ou solicitar revisão

registrarMetricaSemSegredo()
retornar dados
~~~

## Saídas estruturadas

Peça esquema claro e valide no backend. Um modelo pode gerar JSON quase correto, campo extra ou valor inesperado. O seu código deve ser a autoridade sobre o formato e as permissões.

## Custo e desempenho

- Envie apenas contexto relevante.
- Defina limites de tamanho de entrada e saída.
- Faça cache quando for apropriado e permitido.
- Prefira modelos menores para tarefas simples, após testar qualidade.
- Monitore tokens, erros, latência e taxa de fallback.

## Testes necessários

Teste entrada vazia, muito longa, linguagem inesperada, conteúdo malicioso, dados faltantes, JSON inválido, timeout, limite de taxa e resposta sem evidência. Para sistemas que tomam decisões, mantenha revisão humana em pontos críticos.

Conecte este capítulo a [RAG](./21-rag-e-bases-de-conhecimento.md), [Automações](./22-automacoes-com-ia.md) e [Segurança](./18-seguranca-e-privacidade.md).
