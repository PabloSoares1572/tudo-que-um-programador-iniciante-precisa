# Troubleshooting do Windows

Use o mesmo método: descreva o sintoma, preserve dados, colete evidências, teste uma hipótese por vez e confirme a solução.

## PC não inicia

**Possíveis causas:** alimentação, periférico, disco, boot alterado, atualização, driver ou corrupção.  
**Diagnóstico:** remova periféricos não essenciais, confira tela/LEDs, abra Boot Menu e verifique se Windows Boot Manager aparece.  
**Solução segura:** use Ambiente de Recuperação do Windows e documentação oficial; não apague partições nem use comandos de boot aleatórios.  
**Confirmação:** duas inicializações completas sem pendrive.  
**Desfazer:** se uma alteração de firmware causou o problema, restaure apenas a configuração anotada anteriormente.

## Sem internet ou Wi‑Fi

**Possíveis causas:** modo avião, roteador, driver, DNS, VPN, economia de energia.  
**Diagnóstico:** teste outro dispositivo/rede, cabo Ethernet, status do adaptador e data/hora.  
**Solução:** reinicie adaptador/roteador, rode Windows Update, instale driver oficial do modelo.  
**Confirmação:** navegação e resolução de nomes funcionam após reiniciar.  
**Desfazer:** remova driver novo se o problema começou logo depois, usando ponto de restauração/driver anterior quando apropriado.

## Áudio, Bluetooth ou segundo monitor não funcionam

**Possíveis causas:** seleção de saída errada, cabo/porta, driver, atualização, dispositivo desligado.  
**Diagnóstico:** teste dispositivo em outra porta/equipamento; confirme saída selecionada e Gerenciador de Dispositivos.  
**Solução:** atualize/reinstale driver oficial e teste sem dock/adaptador intermediário.  
**Confirmação:** o dispositivo aparece e funciona após novo boot.

## Disco ou pendrive não aparece

**Possíveis causas:** porta, cabo, energia, letra de unidade, partição, falha física.  
**Diagnóstico:** confira Gerenciamento de Disco sem inicializar/formatar automaticamente; teste outro cabo/porta.  
**Solução:** se houver dados importantes, pare antes de criar partição/formato e faça recuperação profissional se necessário.  
**Confirmação:** unidade aparece com tamanho/arquivos esperados.

## Atualização falhou

**Diagnóstico:** anote código, horário, espaço livre e última mudança.  
**Solução:** reinicie, garanta espaço/energia/rede, use solucionador oficial e consulte histórico.  
**Evite:** apagar pastas do sistema ou usar scripts de “reset total” sem backup e entendimento.

Veja também [Formatar PC](../FORMATAR-PC.md) e [Segurança](./06-seguranca.md).
