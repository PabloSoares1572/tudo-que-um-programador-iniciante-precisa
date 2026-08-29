# Otimização Linux baseada em medição

## Medição primeiro

Defina um sintoma mensurável: boot lento, jogo com travadas, bateria baixa, disco cheio, uso alto de RAM ou ventoinha constante. Registre condição, ferramenta, valor e teste repetível antes de mudar.

## Checklist por recurso

| Área | Verifique | Evite |
| --- | --- | --- |
| Atualizações | Kernel, drivers, bugs corrigidos | Bloquear atualização sem plano |
| GPU | Driver recomendado pela distro/fabricante | Misturar drivers manualmente |
| RAM/swap | Processo, memória, zram e pressão | Desativar swap por mito |
| SSD | Espaço, saúde, TRIM conforme suporte | Rodar “otimizador” desconhecido |
| Boot | Serviços e dependências reais | Desabilitar serviços aleatórios |
| Bateria | Perfil de energia, brilho, GPU, processos | Copiar tune de outro notebook |
| Jogos | Driver, Proton/Steam, temperatura, I/O | Prometer FPS com comando universal |

## Análise de gargalo

1. Reproduza o problema.
2. Observe CPU, RAM, disco, rede e temperatura.
3. Liste mudanças recentes.
4. Teste uma intervenção reversível.
5. Compare mesma carga antes/depois.
6. Mantenha somente mudança que melhorou sem efeito colateral.

## Serviços

Um serviço usa recurso porque oferece função. Antes de parar/desabilitar, veja `systemctl status`, dependências e se ele é necessário em boot, rede, áudio, impressão ou segurança. Se tiver dúvida, não desabilite.
