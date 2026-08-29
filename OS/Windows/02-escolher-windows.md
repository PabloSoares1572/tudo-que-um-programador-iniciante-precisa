# Qual Windows escolher?

## Regra geral

Para uso conectado à internet, prefira versão ainda suportada pelo fabricante e compatível com seu hardware. A decisão entre Home e Pro deve seguir recurso necessário, não promessa de desempenho mágico.

## Recomendações por cenário

| Cenário | Direção recomendada | Por quê |
| --- | --- | --- |
| Usuário comum | Windows suportado, Home ou Pro conforme necessidade | Compatibilidade e manutenção simples |
| Jogos | Windows suportado + drivers oficiais de GPU | Compatibilidade de jogos, anti-cheat e drivers importam mais que edição |
| Programação | Windows suportado; Pro pode ajudar se você usar Hyper-V, políticas ou BitLocker | Ferramentas de desenvolvimento funcionam em ambas; defina necessidade real |
| Notebook | Versão suportada e drivers do fabricante | Bateria, Wi‑Fi, áudio e firmware dependem mais dos drivers |
| Empresa | Edição/licença definida pela organização | Administração, identidade e segurança exigem política corporativa |
| Desenvolvimento | Windows suportado + VM/WSL quando necessário | Priorize RAM, SSD e virtualização compatível |
| Máquina virtual | Edição/licença compatível com o hipervisor e o uso | Requisitos da VM são independentes do host em vários pontos |
| Workstation | Pro ou edição corporativa apenas se recursos concretos justificarem | Hardware e carga de trabalho vêm primeiro |
| PC antigo | Não force versão sem suporte; avalie hardware, Linux leve ou manutenção | Bypass de requisito pode reduzir segurança e suporte |
| Privacidade | Configuração consciente, conta e permissões revisadas | Não existe edição que dispense atualizações e boas práticas |
| Administração de sistemas | Pro/Enterprise conforme ambiente e licença | Ferramentas e políticas corporativas podem ser necessárias |
| Servidor | Windows Server quando o papel for servidor Windows | Windows Desktop não substitui produto/licenciamento de servidor |

## Windows 11 — requisitos gerais conhecidos

A Microsoft lista, entre os requisitos gerais, processador compatível de 64 bits com dois ou mais núcleos, 4 GB de RAM, 64 GB de armazenamento, firmware UEFI com capacidade de Secure Boot e TPM 2.0. Há detalhes de CPU, edição e conectividade na [página oficial](https://www.microsoft.com/windows/windows-11-specifications).

> ⚠️ Não use métodos de contorno de requisitos como solução padrão. Eles podem afetar suporte, atualizações, estabilidade e segurança. Primeiro confirme se TPM/Secure Boot estão apenas desativados e se o fabricante oferece suporte ao seu modelo.

## Escolha rápida

1. Confirme suporte e requisitos.
2. Escolha edição pela funcionalidade necessária.
3. Confira licença e compatibilidade de programas.
4. Faça backup antes de upgrade ou instalação limpa.
5. Se o objetivo for aprender Linux, considere [dual boot](../DUAL-BOOT.md) ou máquina virtual.
