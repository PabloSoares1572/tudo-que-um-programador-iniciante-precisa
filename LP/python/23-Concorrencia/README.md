# 23 — Concorrência, threads, processos e async

> 🔴 **Avançado**

Concorrência é lidar com mais de uma tarefa em progresso; paralelismo é executar trabalho ao mesmo tempo em mais de um recurso de processamento. São conceitos relacionados, mas não sinônimos.

## Escolha pelo tipo de trabalho

| Situação | Caminho comum |
| --- | --- |
| muitas esperas de rede/arquivo compatível | \`asyncio\` ou threads, conforme biblioteca |
| CPU pesada | \`multiprocessing\` ou processamento externo |
| biblioteca bloqueante simples | thread pode ser adequada |
| aplicação web moderna | siga o modelo do framework e meça |

## Threads

Threads compartilham memória do processo, exigindo cuidado com estado mutável, locks e condições de corrida. Não compartilhe uma lista/dicionário por várias threads sem uma política clara.

## Processos

Processos isolam memória e podem usar mais de um núcleo em tarefas CPU-bound, mas têm custo de criação e comunicação. Objetos enviados entre processos precisam ser serializáveis em vários cenários.

## Async

\`async\`/\`await\` permite cooperar durante esperas. Não torna automaticamente uma função rápida nem paralela em CPU.

\`\`\`python
import asyncio

async def buscar_dado():
    await asyncio.sleep(0.1)
    return "pronto"

resultado = asyncio.run(buscar_dado())
print(resultado)
\`\`\`

## Próximo

- [Decisão prática e erros comuns](./01-escolha-e-armadilhas.md)

← [Web](../22-Web/README.md) | [Performance →](../24-Performance/README.md)

