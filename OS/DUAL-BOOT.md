# Dual boot Windows + Linux

> 🟡 **Nível:** intermediário.  
> ⚠️ **Risco:** uma escolha errada no particionamento pode apagar o Windows, Linux ou arquivos pessoais. Faça backup e tenha a chave de recuperação do BitLocker antes de começar.

## O que é dual boot?

Dual boot é ter dois sistemas operacionais instalados no mesmo computador e escolher qual iniciar ao ligar. O caso mais comum é Windows + Linux.

| Vantagens | Desvantagens |
| --- | --- |
| Desempenho nativo em cada sistema | Exige reiniciar para trocar de sistema |
| Permite manter programas exclusivos do Windows | Particionamento e boot exigem cuidado |
| Bom para aprender Linux gradualmente | Atualizações/firmware podem mudar a ordem de boot |
| Usa hardware real, inclusive GPU | Espaço em disco é dividido |

## Alternativas

- **Máquina virtual:** Linux dentro de janela no Windows; ótima para estudar terminal sem mexer no boot, mas tem menor acesso direto à GPU/hardware.
- **Live USB:** inicia Linux pelo pendrive sem instalar; bom para testar compatibilidade.
- **WSL:** ambiente Linux integrado ao Windows para terminal/desenvolvimento; não substitui um desktop Linux completo em todos os casos.
- **Segundo computador/SSD externo:** reduz risco de coexistência no mesmo disco, mas ainda requer backup e atenção ao boot.

## Conceitos que você precisa conhecer

| Item | Por que importa |
| --- | --- |
| UEFI + GPT | É a combinação mais comum em PCs atuais e facilita coexistência moderna |
| EFI System Partition (ESP) | Guarda entradas/arquivos de boot para os sistemas |
| Bootloader | Programa que apresenta ou encaminha a escolha de sistema; GRUB é comum no Linux |
| BitLocker | Criptografia do Windows que pode pedir chave de recuperação após mudanças de boot/firmware |
| Fast Startup | Pode deixar partições Windows em estado híbrido; desligamento completo evita risco ao acessar dados compartilhados |
| Espaço não alocado | Espaço livre sem partição onde o Linux pode ser instalado |

## Antes de começar

- [ ] Backup testado de arquivos importantes.
- [ ] Chave de recuperação de BitLocker salva fora do computador, se houver criptografia.
- [ ] Windows atualizado e inicializando normalmente.
- [ ] Espaço livre suficiente para o Linux, arquivos e atualizações.
- [ ] ISO baixada da fonte oficial e pendrive bootável testado.
- [ ] Você identificou qual SSD/HDD contém o Windows.
- [ ] Você sabe abrir o Boot Menu do seu PC.
- [ ] Você leu o guia da distribuição escolhida e sabe se ela suporta Secure Boot no seu cenário.

## Preparar Windows sem apagar nada

1. Faça backup e desligue aplicativos/sincronizações importantes.
2. Verifique se BitLocker/criptografia está ativa e guarde a chave de recuperação. Não desative criptografia apenas por hábito; siga a documentação da distribuição se alguma etapa exigir suspensão temporária.
3. Desative o **Fast Startup** e faça um desligamento completo antes de acessar uma partição NTFS pelo Linux. Isso reduz risco de corrupção por estado de hibernação híbrida.
4. Use o Gerenciamento de Disco do Windows para **reduzir a partição do Windows** e criar espaço não alocado. Não crie uma partição NTFS nova nesse espaço se o instalador Linux vai cuidar da instalação.
5. Não apague a partição EFI, Recovery ou a partição principal do Windows.

> ⚠️ Em computadores com Intel RST/RAID, alterar para AHCI sem preparo pode fazer o Windows não iniciar. Pesquise o procedimento específico do fabricante e crie plano de reversão antes de mudar qualquer modo de armazenamento.

## Cenário A — Windows instalado primeiro, Linux depois

Este é o cenário recomendado para a maioria das pessoas.

1. No Windows, reduza a partição e deixe **espaço não alocado**.
2. Inicie o pendrive Linux pela entrada UEFI do Boot Menu.
3. Se possível, teste no modo live: Wi‑Fi, áudio, teclado, touchpad, vídeo e armazenamento.
4. No instalador, escolha “instalar ao lado” somente se ele identificar corretamente Windows e espaço livre.
5. Se optar por particionamento manual, selecione exclusivamente o espaço não alocado. Crie a partição Linux e, se necessário, swap; use a partição EFI existente **sem formatá-la**, quando o guia da distribuição assim orientar.
6. Confirme o resumo final antes de iniciar. A tela não pode listar a partição Windows como alvo de formatação.
7. Após o primeiro boot, confira que Windows e Linux aparecem no menu; se não aparecerem, consulte recuperação abaixo.

## Cenário B — Linux instalado primeiro, Windows depois

É mais arriscado para iniciantes porque instaladores do Windows podem priorizar o Windows Boot Manager. Antes, mantenha um Live USB da distribuição e backup dos dados Linux.

1. Reserve espaço não alocado para Windows; não use uma partição Linux existente.
2. Inicie o instalador Windows em modo UEFI.
3. Direcione a instalação apenas ao espaço livre planejado.
4. Depois, o computador pode iniciar direto no Windows. Entre no firmware/Boot Menu e teste a entrada Linux.
5. Se precisar reparar o bootloader Linux, siga exclusivamente o procedimento oficial da distribuição, usando live USB e confirmando o disco/partição EFI.

## Cenário C — dois SSDs diferentes

É o cenário mais simples de diagnosticar. Instale cada sistema no seu SSD, mas saiba que ambos podem usar a mesma ESP ou ESPs separadas, conforme firmware/instalador. Durante a instalação, desconectar temporariamente o SSD que não será alterado reduz o risco de apagar ou colocar boot no disco errado — desde que você saiba abrir o equipamento sem violar garantia.

Depois, use o Boot Menu ou o firmware para escolher o sistema. É normal que o menu de uma distribuição não liste automaticamente todos os sistemas até ser configurado/atualizado conforme a documentação dela.

## Cenário D — notebook, Secure Boot e criptografia

- Faça backup de chaves de recuperação antes de mudar firmware ou boot.
- Mantenha UEFI/GPT em vez de voltar para Legacy/CSM sem necessidade.
- Secure Boot pode funcionar com distribuições que o suportam; não desative por reflexo. Se tiver problema, consulte a documentação específica da distribuição e do fabricante.
- Desative Fast Startup antes de compartilhar acesso a NTFS.
- Não monte em modo de escrita uma partição Windows hibernada.

## Relógio diferente entre Windows e Linux

Os sistemas podem interpretar o relógio de hardware de maneira diferente. Se a hora muda toda vez que você troca de SO, ajuste a configuração no sistema escolhido seguindo documentação atual, em vez de alterar fuso horário às cegas. O importante é escolher um comportamento consistente e verificar após reiniciar nos dois sistemas.

## Acesso a arquivos entre sistemas

- NTFS costuma ser o ponto de compartilhamento mais prático para dados, mas o Windows precisa estar totalmente desligado (sem Fast Startup/hibernação) antes de o Linux escrever nela.
- ext4 não tem suporte nativo completo no Windows; não dependa dele para compartilhar arquivos sem ferramenta e sem backup.
- Para arquivos críticos, cópia externa ou nuvem pode ser mais segura que editar diretamente entre sistemas.

## Recuperação de boot — primeiro proteja dados

Antes de “consertar GRUB” ou reescrever bootloader, use um live USB para copiar arquivos importantes. Reparos de boot podem ser reversíveis, mas tentativas aleatórias de partição não são.

### Windows não aparece no menu

1. Confira no firmware se **Windows Boot Manager** ainda aparece.
2. Tente iniciá-lo pelo Boot Menu; isso verifica se Windows ainda está intacto.
3. No Linux, siga a documentação da distribuição para atualizar o bootloader/entrada; não use comandos genéricos copiados de outro sistema.
4. Se Windows não inicia, use o Ambiente de Recuperação do Windows e documentação oficial antes de mexer na partição EFI.

### Linux não aparece ou PC abre direto no Windows

1. Abra o Boot Menu e procure a entrada da distribuição/UEFI.
2. Verifique se o SSD Linux é reconhecido pelo firmware.
3. Confira se uma atualização de firmware/Windows alterou a prioridade de boot.
4. Inicie live USB e use o guia oficial da distribuição para reparar o bootloader, conferindo `lsblk -f` e a partição EFI antes de qualquer escrita.

### GRUB aparece, mas o sistema não inicia

Não reinstale o sistema imediatamente. Anote a mensagem, teste iniciar por opções avançadas e consulte logs/recovery da distribuição. Um problema de kernel, driver ou `fstab` pode ter conserto sem apagar dados.

## Como confirmar que deu certo

- Ambos os sistemas aparecem no Boot Menu ou bootloader.
- Cada sistema inicia duas vezes seguidas sem pendrive.
- Relógio, rede, áudio e armazenamento funcionam.
- Você consegue desligar totalmente o Windows antes de acessar dados NTFS pelo Linux.
- BitLocker não está pedindo chave inesperadamente; se pedir, use a chave legítima salva e investigue a mudança de boot/firmware antes de repetir.

## Próximos passos

- [Formatar o PC](./FORMATAR-PC.md)
- [Primeiros passos no Linux](./Linux/01-primeiros-passos.md)
- [Instalação geral de distribuições](./Linux/Distribuicoes/INSTALACAO-GERAL.md)
