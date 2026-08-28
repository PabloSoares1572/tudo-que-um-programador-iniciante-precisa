# 02 — Como modelos generativos funcionam

## A ideia central: prever a próxima parte

Modelos de linguagem são treinados para prever a próxima unidade de texto. Dado “O Brasil fica na América…”, uma continuação provável é “do Sul”. Repetindo esse processo muitas vezes, eles conseguem formar frases, código, listas e explicações.

Isso não significa que o modelo “consultou uma enciclopédia” naquele instante. Em muitos produtos, a pesquisa na web é uma ferramenta separada e precisa ser indicada como tal.

## Do dado à resposta

1. **Coleta e preparação:** exemplos de texto, código, imagens ou áudio são transformados em formatos que o modelo consegue processar.
2. **Treinamento:** o modelo ajusta muitos parâmetros para reconhecer padrões.
3. **Alinhamento:** são aplicadas técnicas para tornar respostas mais úteis, seguras e obedientes a instruções.
4. **Inferência:** quando você envia um prompt, o modelo gera a resposta token por token.

## Por que duas respostas podem ser diferentes?

Alguns modelos usam uma dose de aleatoriedade controlada. Configurações com nomes como **temperature** influenciam a variedade das respostas: menor tende a ser mais previsível; maior pode trazer mais alternativas, mas também mais risco de sair do foco.

Não trate uma configuração isolada como “botão de criatividade”. Objetivo, contexto e exemplos normalmente têm impacto maior.

## Capacidade não é garantia

Um modelo pode:

- explicar bem um assunto e errar uma data;
- escrever código plausível que não roda;
- citar uma fonte inexistente;
- seguir instruções conflitantes de modo imperfeito;
- perder detalhes em conversas longas.

Por isso, a pergunta correta não é “a IA sabe?”, mas “como valido este resultado?”.

## Prompt, contexto e ferramenta são coisas diferentes

| Elemento | Função | Exemplo |
| --- | --- | --- |
| Prompt | Pedido que você escreve | “Crie uma tabela comparativa” |
| Contexto | Informação fornecida para a tarefa | Texto, regras, público, arquivos |
| Ferramenta | Recurso externo usado durante a execução | Pesquisa, calculadora, editor de arquivos |
| Memória | Preferências ou dados mantidos por uma plataforma | Pode variar por produto e configuração |

Uma resposta só deve afirmar que pesquisou, leu um arquivo ou executou um cálculo quando a ferramenta realmente foi usada e o resultado estiver disponível.

## Exemplo: mesma tarefa, resultados diferentes

❌ **Pedido vago**

> Faça um texto sobre segurança digital.

✅ **Pedido definido**

> Escreva uma introdução de 180 a 220 palavras sobre segurança digital para alunos iniciantes. Explique phishing, senhas fortes e autenticação em dois fatores. Use linguagem simples, três subtítulos e não invente estatísticas. Ao final, crie uma checklist de cinco ações.

O segundo pedido reduz decisões escondidas: define público, tamanho, tópicos, formato e uma restrição importante.

## Quando usar outro método

- **Cálculo exato:** use calculadora, planilha ou código e revise a fórmula.
- **Fato atual:** consulte fonte recente e confiável.
- **Regra jurídica, médica ou financeira:** use fonte oficial e profissional habilitado quando necessário.
- **Decisão importante:** trate a IA como apoio para opções e perguntas, não como autoridade final.

Leia também: [Limitações e alucinações](./17-limitacoes-e-alucinacoes.md) e [Pesquisa e verificação](./12-pesquisa-e-verificacao.md).
