# Formatar um PC com segurança

> 🟢 **Nível:** iniciante, com partes 🟡 intermediárias.  
> ⚠️ **Risco principal:** selecionar o disco/partição errada pode apagar dados de forma difícil ou impossível de recuperar.

## O que significa “formatar”?

No uso cotidiano, “formatar o PC” costuma significar apagar ou reinstalar o sistema operacional para começar de novo. Tecnicamente, formatar uma partição prepara nela um sistema de arquivos; reinstalar pode preservar ou recriar partições, dependendo da escolha.

| Ação | O que acontece | Quando usar |
| --- | --- | --- |
| Limpeza de arquivos | Remove arquivos temporários ou programas | Sistema com pouco espaço ou lentidão leve |
| Redefinição/reinstalação | Reinstala o Windows por recurso de recuperação | Problemas de sistema sem troca de disco |
| Instalação limpa | Apaga a partição/sistema escolhido e instala do zero | Infecção, corrupção grave, troca de dono ou mudança de SO |
| Formatação de unidade externa | Cria sistema de arquivos em pendrive/HDD externo | Quando o dispositivo será reutilizado |

## Quando formatar — e quando não formatar

**Considere reinstalar** quando há erros recorrentes, malware confirmado, sistema muito corrompido, troca de armazenamento ou necessidade de instalação limpa.

**Não formate como primeira reação** a um problema simples: falta de espaço, um programa com erro, Wi‑Fi com driver ausente, cabo defeituoso ou conta de usuário corrompida podem ter solução menos invasiva. Primeiro faça diagnóstico e backup.

## CHECKLIST ANTES DE FORMATAR

Marque cada item. Se um item não se aplica, registre o motivo.

- [ ] Copiei documentos, fotos, vídeos, downloads e área de trabalho para local diferente do disco que será apagado.
- [ ] Confirmei se meus jogos salvam na nuvem; exportei saves locais importantes.
- [ ] Exporte favoritos, senhas e códigos de recuperação do navegador/gerenciador de senhas.
- [ ] Guardei códigos de autenticação em duas etapas e confirmei acesso ao e-mail principal.
- [ ] Anotei contas, licenças de software e chaves de produto legítimas.
- [ ] Verifiquei se o Windows usa criptografia/BitLocker e salvei a chave de recuperação fora do PC.
- [ ] Baixei, em local seguro, drivers de rede/chipset/GPU se o fabricante os disponibilizar.
- [ ] Tenho pendrive vazio dedicado à instalação (recomendado: 8 GB ou mais; confirme a exigência da ferramenta/ISO).
- [ ] Conheço qual disco contém o sistema e quais discos têm dados que não podem ser tocados.
- [ ] Desconectei unidades externas desnecessárias para reduzir o risco de selecionar a unidade errada.
- [ ] Tenho energia estável; em notebook, carregador conectado.
- [ ] Li o fluxo completo antes de apagar qualquer partição.

## Backup que realmente permite voltar

Um backup só existe se você consegue localizar e abrir o arquivo em outro dispositivo. Use pelo menos duas cópias para dados importantes: uma externa e, se fizer sentido, uma nuvem confiável.

### O que costuma ser esquecido

- pastas Área de Trabalho, Documentos, Imagens, Vídeos e Downloads;
- perfis de navegador, favoritos e extensões;
- bancos de dados locais, projetos, máquinas virtuais e chaves SSH;
- arquivos de aplicativos de criação, presets e fontes;
- saves de jogos fora da nuvem;
- certificados, tokens de autenticação e chaves de recuperação;
- e-mails arquivados localmente e arquivos sincronizados que ainda não terminaram de subir.

## ISO, imagem de sistema e pendrive bootável

- **ISO:** arquivo que representa o conteúdo de uma mídia de instalação.
- **Imagem de sistema:** termo amplo para cópia/instalador do sistema; uma ISO é um tipo de imagem.
- **Pendrive bootável:** pendrive preparado para iniciar o computador e carregar o instalador. Apenas copiar a ISO como arquivo normalmente não basta.

### Origem legítima

Baixe sistema e verificações somente em site oficial. Projetos como Debian, Fedora e Arch publicam checksums/assinaturas; use-os quando o projeto fornecer instruções. A [página de referências oficiais](./REFERENCIAS-OFICIAIS.md) centraliza pontos de partida.

Evite ISOs “otimizadas”, “pré-ativadas”, “lite”, packs de drivers desconhecidos ou links de terceiros. Eles podem conter malware, alterações invisíveis e problemas de licença.

### Ferramentas comuns

| Ferramenta | Uso | Observação |
| --- | --- | --- |
| Ferramenta oficial da Microsoft | Cria/baixa mídia oficial do Windows | Melhor ponto de partida para Windows |
| [Rufus](https://rufus.ie/) | Grava uma imagem no pendrive no Windows | Confirme cuidadosamente o pendrive selecionado |
| [Ventoy](https://www.ventoy.net/) | Prepara pendrive para iniciar várias ISOs | Instalar Ventoy também altera o dispositivo escolhido |
| Ferramenta da distribuição | Algumas distribuições oferecem gravador próprio | Prefira quando recomendado pela documentação oficial |

> ⚠️ Criar pendrive bootável **apaga o pendrive escolhido**. Remova outros pendrives antes e confira tamanho/modelo do dispositivo três vezes.

## BIOS, UEFI e Boot Menu — o mínimo necessário

- **BIOS/UEFI:** firmware que inicia antes do sistema operacional. Em PCs modernos, o termo correto geralmente é UEFI.
- **Boot Menu:** menu temporário para escolher de qual dispositivo iniciar.
- **Ordem de boot:** lista persistente de prioridade de inicialização.
- **Secure Boot:** recurso de UEFI que verifica componentes de boot compatíveis.
- **TPM:** componente de segurança usado, entre outras coisas, por recursos do Windows e criptografia.
- **AHCI:** modo comum de controlador SATA; mudar modo de armazenamento sem preparo pode impedir um sistema existente de iniciar.
- **GPT/MBR:** estilos de tabela de partições. UEFI moderno normalmente trabalha com GPT.

Teclas comuns para entrar no firmware ou menu: `Del`, `F2`, `F10`, `F12` e `Esc`, mas variam por fabricante. Leia a mensagem de inicialização ou o manual do modelo. Prefira o **Boot Menu temporário** a mudar a ordem permanente.

> ⚠️ Não altere aleatoriamente Secure Boot, CSM/Legacy, modo SATA/AHCI, TPM ou ordem de boot. Anote a configuração original e mude uma opção por vez, somente quando um guia compatível com seu computador pedir.

## Discos, partições e sistemas de arquivos

| Termo | Explicação simples |
| --- | --- |
| Disco | Unidade física: HDD, SSD SATA ou SSD NVMe |
| Partição | Divisão lógica de um disco |
| Volume | Parte utilizável apresentada ao sistema, geralmente associada a uma partição |
| Espaço não alocado | Parte do disco ainda sem partição |
| EFI | Pequena partição usada pelo UEFI para arquivos de inicialização |
| Recovery | Partição de recuperação do fabricante ou do Windows |
| NTFS | Sistema de arquivos típico do Windows |
| FAT32 | Compatível e comum em mídias EFI, com limitações de tamanho de arquivo |
| exFAT | Bom para arquivos grandes em unidades compartilhadas; não é sistema Linux completo |
| ext4 | Sistema de arquivos muito comum em Linux |
| swap | Espaço de apoio à memória no Linux; pode ser arquivo ou partição |

Antes de apagar, compare **capacidade**, **nome do modelo**, **partições existentes** e conteúdo. Não se baseie apenas em “Disco 0” ou “Disco 1”.

## Fluxo de instalação limpa

~~~text
Backup
↓
Baixar sistema em fonte oficial
↓
Verificar arquivo quando houver instrução oficial
↓
Criar pendrive bootável
↓
Abrir Boot Menu
↓
Iniciar instalador
↓
Confirmar disco e partições
↓
Instalar
↓
Primeiro boot
↓
Atualizações, drivers e programas
↓
Restaurar arquivos e configurar backup
~~~

### Durante o instalador

1. Confirme idioma, teclado e fuso horário.
2. Escolha cuidadosamente **instalação limpa** ou **instalação ao lado**; não suponha que o instalador escolheu o disco correto.
3. Quando houver mais de um disco, confira capacidade/modelo. Desconectar unidades de dados antes pode reduzir risco.
4. Leia a tela final de confirmação. Ela normalmente diz quais partições serão apagadas.
5. Não desligue o PC enquanto o instalador escreve dados, salvo se a própria tela instruir.

## Depois da instalação

1. Conecte à rede e atualize o sistema.
2. Instale drivers prioritariamente via Windows Update, fabricante do notebook/placa-mãe e fabricante da GPU quando necessário.
3. Ative o sistema de forma legítima com licença válida; não use ativadores ou scripts de origem duvidosa.
4. Instale programas de fontes oficiais.
5. Restaure arquivos em etapas e faça varredura de arquivos suspeitos.
6. Crie ponto/imagem de recuperação e configure backup recorrente.
7. Só então descarte a cópia antiga, após confirmar que tudo abriu.

## Problemas frequentes

### O pendrive não aparece no Boot Menu

**Possíveis causas:** mídia mal gravada, porta USB, modo UEFI/Legacy incompatível ou firmware bloqueando o boot.  
**Diagnóstico:** teste o pendrive em outro computador, recrie a mídia com ISO oficial e confira se selecionou a entrada UEFI adequada.  
**Solução segura:** recrie a mídia; não desative proteções permanentemente sem entender o motivo.

### O disco não aparece no instalador

**Possíveis causas:** driver de armazenamento, Intel RST/RAID, cabo/SSD com problema, modo do controlador ou falha de hardware.  
**Diagnóstico:** confirme se o disco aparece no firmware e em outro sistema.  
**Solução:** pesquise o modelo do computador na documentação oficial antes de mudar RAID/RST/AHCI; a mudança errada pode tornar o sistema instalado não inicializável.

### O sistema reinicia no pendrive de novo

Remova o pendrive após a primeira etapa se o instalador pedir ou selecione o disco interno no Boot Menu. Não apague partições adicionais achando que a instalação “não funcionou” antes de verificar a ordem de boot.

## Próximos guias

- Para Windows: [Instalação e reinstalação](./Windows/03-instalacao-e-reinstalacao.md).
- Para Linux: [Primeiros passos](./Linux/01-primeiros-passos.md).
- Para dois sistemas: [Dual boot](./DUAL-BOOT.md).
