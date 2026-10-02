# Instalação e verificação

## Windows

1. Baixe Python pelo [site oficial](https://www.python.org/downloads/) ou siga a [documentação para Windows](https://docs.python.org/3/using/windows.html).
2. Instale uma versão Python 3 atual e suportada.
3. Abra PowerShell ou Prompt de Comando e teste:

```text
py --version
py -m pip --version
```

Em instalações modernas, `py` seleciona o interpretador. Se tiver várias versões, `py -3.14 --version` é um exemplo de seleção explícita quando essa versão existir.

## Linux

Muitas distribuições já incluem `python3`. Confirme:

```text
python3 --version
python3 -m pip --version
```

Instale Python e `pip` somente pelo gerenciador de pacotes da distribuição, seguindo a documentação dela. Evite substituir o Python usado pelo sistema com `sudo pip install`; projetos devem usar ambientes virtuais.

## macOS

Use a documentação oficial para macOS ou um gerenciador de pacotes confiável conforme sua necessidade. Confirme pelo terminal:

```text
python3 --version
python3 -m pip --version
```

## PATH, em linguagem simples

`PATH` é uma lista de pastas em que o sistema procura programas quando você digita um comando. Se `python` ou `py` não for reconhecido, não baixe arquivos aleatórios: confira a instalação e a documentação da sua plataforma.

## Confirmação

Você terminou quando o terminal mostra uma versão Python 3 e o comando de `pip` correspondente responde sem erro.

← [Ambiente](./README.md) | [Editor e terminal →](./02-editor-ide-e-terminal.md)
