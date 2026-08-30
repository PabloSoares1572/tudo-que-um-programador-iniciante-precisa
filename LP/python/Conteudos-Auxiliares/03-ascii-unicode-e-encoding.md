# ASCII, Unicode e encoding

Computadores guardam números. **Unicode** define pontos de código para caracteres de muitos idiomas; **UTF-8** é uma codificação comum para transformar esses caracteres em bytes.

Python 3 trabalha bem com texto Unicode, mas arquivos e comunicação externa ainda precisam de encoding explícito:

\`\`\`python
with open("texto.txt", encoding="utf-8") as arquivo:
    texto = arquivo.read()
\`\`\`

ASCII é subconjunto histórico limitado. Se acentos ficam quebrados, descubra a codificação real do arquivo em vez de remover caracteres ou tentar codecs aleatórios.

