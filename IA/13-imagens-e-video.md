# 13 — IA para imagens e vídeos

## Descreva a cena, não use “comandos mágicos”

Palavras como “cinematográfico”, “realista” ou “alta qualidade” podem orientar um estilo, mas não são comandos universais. Cada ferramenta interpreta linguagem, imagens de referência e configurações de maneira diferente. Consulte a documentação da plataforma para recursos específicos.

## Estrutura de briefing visual

| Elemento | Perguntas úteis |
| --- | --- |
| Assunto | Quem ou o que aparece? |
| Ação | O que está acontecendo? |
| Ambiente | Onde e em qual período? |
| Composição | Enquadramento, posição e foco? |
| Estilo | Foto, ilustração, 3D, editorial? |
| Luz e cor | Natural, estúdio, noturna, paleta? |
| Formato | Horizontal, vertical, quadrado, proporção? |
| Restrições | O que não pode aparecer? |

## Prompt de imagem

~~~text
Crie uma [foto/ilustração] de [assunto] em [ambiente].
Composição: [enquadramento e posição].
Luz: [tipo de luz]. Paleta: [cores].
Estilo visual: [referência descritiva, sem copiar artista vivo].
Formato: [proporção].
Evite: [elementos, texto, erros anatômicos ou marcas].
~~~

## Prompt ruim x melhorado

❌ “Faça uma imagem bonita de uma cafeteria.”

✅ “Crie uma fotografia editorial de uma cafeteria pequena em manhã chuvosa. Enquadramento na altura da mesa, xícara em foco no primeiro plano, janela com gotas desfocada ao fundo, luz natural suave e paleta quente. Formato vertical 4:5. Sem texto, logotipos ou pessoas reconhecíveis.”

## Vídeo: acrescente tempo e movimento

> Gere uma cena de 6 segundos: câmera avança lentamente por uma mesa de trabalho organizada, com luz de fim de tarde entrando pela janela. Movimento suave, sem cortes, foco mudando do caderno para o monitor. Formato vertical 9:16. Sem texto ou marca.

Descreva duração, câmera, ação, transição e o que precisa permanecer consistente entre cenas.

## Referências e identidade

- Use imagens próprias ou referências para as quais você tem permissão.
- Não prometa preservar perfeitamente rosto, corpo ou marca sem validar a ferramenta e o resultado.
- Evite usar imagem de pessoa real sem consentimento, especialmente em contexto enganoso ou sensível.
- Respeite direitos autorais, termos de uso e regras da plataforma.

## Itere em uma variável por vez

Primeiro corrija composição; depois luz; depois estilo. Mudar tudo ao mesmo tempo dificulta descobrir o que melhorou.

Biblioteca: [prompts para imagens e vídeos](./exemplos/prompts-imagens-e-videos.md).
