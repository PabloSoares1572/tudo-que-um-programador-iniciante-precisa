# Sistema operacional, processo e thread

O sistema operacional administra memória, CPU, arquivos, rede e dispositivos. Quando você executa Python, o SO cria um **processo** para o interpretador. Um processo pode conter uma ou mais **threads**, que são linhas de execução compartilhando recursos do processo.

Isso explica por que arquivo inexistente, porta ocupada e permissão negada são problemas do ambiente, não necessariamente da sintaxe Python. Também prepara o módulo de concorrência: threads compartilham memória; processos isolam mais, mas custam mais comunicação.

Para aprender comandos e estrutura de Windows/Linux, consulte a seção [OS](../../../OS/README.md) do repositório.
