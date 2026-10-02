# CPython, memória, garbage collection e GIL

## Modelo mental útil

Em CPython, nomes referenciam objetos. Atribuir `b = a` normalmente não cria cópia; os dois nomes podem apontar ao mesmo objeto mutável. Por isso cópias rasas e profundas exigem atenção.

## Coleta de lixo

CPython usa contagem de referências e um coletor para lidar com ciclos. Na maioria dos programas, você não chama `gc.collect()` manualmente. Corrija referências desnecessárias, feche recursos com `with` e meça vazamentos antes de otimizar.

## GIL

O Global Interpreter Lock do CPython limita a execução simultânea de bytecode Python por múltiplas threads no mesmo processo tradicional. Isso não significa que threads são inúteis: operações de I/O, como rede e arquivos, podem se beneficiar. Para CPU pesada, processos ou extensões apropriadas podem ser melhores. A decisão depende de medição e do tipo de trabalho.

## Introspecção responsável

`dir(obj)`, `help(obj)` e `inspect` ajudam a explorar objetos. Não dependa de atributos internos com `_` como se fossem API estável; leia a documentação pública da biblioteca.

← [Data model](./01-data-model-e-dunder.md) | [Type hints →](../15-Type-Hints/README.md)
