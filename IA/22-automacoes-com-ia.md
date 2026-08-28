# 22 — Automações com IA

## Automação x agente

Uma automação segue fluxo previsível: gatilho → processamento → ação. Um agente pode escolher próximas etapas e ferramentas dentro de regras. Comece por automação simples sempre que o processo puder ser descrito com clareza.

## Arquitetura segura

~~~text
Gatilho → coleta autorizada → validação → IA → revisão/regra → ação → log/alerta
~~~

Exemplo: novo formulário chega → campos são validados → IA classifica o tema → regra verifica confiança → humano aprova casos críticos → sistema cria um rascunho → log registra o resultado.

## Casos de uso

| Fluxo | Papel da IA | Controle necessário |
| --- | --- | --- |
| Triagem de e-mails | Classificar e resumir | Não responder automaticamente a mensagens sensíveis |
| Relatório periódico | Resumir métricas | Conferir dados de origem |
| Atendimento inicial | Rascunhar respostas | Escalonar casos complexos para humano |
| Extração de documentos | Estruturar campos | Validar campos críticos e privacidade |
| Criação de tarefas | Converter texto em checklist | Evitar atribuições inventadas |

## Comece com “human in the loop”

Ponha aprovação humana antes de:

- enviar e-mail, mensagem ou publicação;
- apagar, mover ou editar dados;
- fazer compras ou transações;
- mudar produção;
- aplicar mudanças de código;
- compartilhar informações externas.

## Prompt de classificação

~~~text
Classifique a solicitação em: suporte, financeiro, técnico ou outro.
Retorne JSON com categoria, confiança (0 a 1), resumo e motivo curto.
Se não houver informação suficiente, use categoria "outro" e confiança menor que 0,5.
Não execute ações nem escreva resposta ao cliente.
~~~

## Confiabilidade operacional

- Valide entrada antes de chamar o modelo.
- Defina timeout, retentativa e comportamento de falha.
- Salve logs sem guardar segredos.
- Monitore taxa de erro e casos encaminhados.
- Mantenha opção de desligar o fluxo.
- Teste com dados fictícios e casos extremos.

## Anti-padrão

“Quando chegar qualquer e-mail, deixe a IA decidir e responder tudo” mistura dados não confiáveis, ação externa e risco de alucinação. Prefira classificar, sugerir rascunho e exigir aprovação.

Para integrações por código, veja [APIs de IA](./23-apis-de-ia.md). Para agentes, consulte [Agentes de IA](./20-agentes-de-ia.md).
