# Notas da VersÃ£o â€” Wconect VoIP 1.0.2

## ðŸ”§ CorreÃ§Ã£o importante

Corrigimos um problema que podia travar o aplicativo logo ao abrir,
afetando o funcionamento correto do Ã­cone na bandeja do sistema
(aquele Ã­cone perto do relÃ³gio, usado para abrir ou fechar o Wconect
VoIP). Com essa correÃ§Ã£o, o app abre normalmente e o menu do Ã­cone da
bandeja volta a funcionar como esperado.

---

## ðŸ–¥ï¸ DiÃ¡logo "AtualizaÃ§Ã£o disponÃ­vel"

- Visual reorganizado, mais limpo e alinhado ao restante do app.
- A lista de novidades de cada versÃ£o agora aparece bem formatada,
  item por item.

---

**Wconect VoIP 1.0.2**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**â¬‡ï¸ Baixar a versÃ£o 1.0.2:** [Wconect-VoIP_1.0.2.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.2/Wconect-VoIP_1.0.2.exe)

---

# Notas da VersÃƒÂ£o Ã¢â‚¬â€ Wconect VoIP 1.0.1

## Ã°Å¸â€Â§ CorreÃƒÂ§ÃƒÂµes e melhorias

VersÃƒÂ£o de manutenÃƒÂ§ÃƒÂ£o sobre a base **1.0**, focada em corrigir o
controle de volume do DTMF e em melhorar a experiÃƒÂªncia do popup de
chamada recebida em ambientes com mÃƒÂºltiplos monitores.

---

## Ã°Å¸Å½Å¡Ã¯Â¸Â Volumes

- Corrigida a ordem de aplicaÃƒÂ§ÃƒÂ£o do ganho na porta de DTMF/teste de
  alto-falante (agora alinhada ao mesmo padrÃƒÂ£o jÃƒÂ¡ usado por Toque e
  Ringback), eliminando a inconsistÃƒÂªncia encontrada numa auditoria
  completa dos 4 controles de volume (Toque, Ringback, Chamada, DTMF).

---

## Ã°Å¸â€œÅ¾ Chamada recebida

- O popup de chamada recebida agora abre sempre **centralizado no mesmo
  monitor** em que a janela principal estÃƒÂ¡, mesmo em configuraÃƒÂ§ÃƒÂµes
  multi-monitor.
- Adicionado o logotipo oficial do Wconect no topo do popup.

---

## Ã°Å¸â€ºÂ Ã¯Â¸Â Infraestrutura interna

- Adicionada instrumentaÃƒÂ§ÃƒÂ£o permanente de diagnÃƒÂ³stico do pipeline de
  ÃƒÂ¡udio nativo (PJSIP), ativa somente em builds de desenvolvimento Ã¢â‚¬â€
  sem nenhum impacto na versÃƒÂ£o instalada pelos usuÃƒÂ¡rios.

---

**Wconect VoIP 1.0.1**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**Ã¢Â¬â€¡Ã¯Â¸Â Baixar a versÃƒÂ£o 1.0.1:** [Wconect-VoIP_1.0.1.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.1/Wconect-VoIP_1.0.1.exe)

---

# Notas da VersÃƒÆ’Ã‚Â£o ÃƒÂ¢Ã¢â€šÂ¬Ã¢â‚¬Â Wconect VoIP 1.0

## ÃƒÂ°Ã…Â¸Ã…Â¡Ã¢â€šÂ¬ Bem-vindo ao Wconect VoIP 1.0

ÃƒÆ’Ã¢â‚¬Â° com grande satisfaÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o que apresentamos a primeira versÃƒÆ’Ã‚Â£o oficial do **Wconect VoIP**, um softphone desenvolvido para oferecer uma experiÃƒÆ’Ã‚Âªncia moderna, rÃƒÆ’Ã‚Â¡pida, segura e intuitiva para comunicaÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o corporativa.

Desenvolvido com Flutter e utilizando o PJSIP como motor SIP nativo, o Wconect VoIP foi projetado para oferecer alta qualidade nas chamadas, excelente desempenho e uma base sÃƒÆ’Ã‚Â³lida para futuras evoluÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Âµes.

---

# ÃƒÂ¢Ã…â€œÃ‚Â¨ Novidades da VersÃƒÆ’Ã‚Â£o 1.0

## ÃƒÂ¢Ã‹Å“Ã…Â½ÃƒÂ¯Ã‚Â¸Ã‚Â Telefonia SIP

- Cadastro de contas SIP.
- Registro automÃƒÆ’Ã‚Â¡tico no servidor.
- ReconexÃƒÆ’Ã‚Â£o automÃƒÆ’Ã‚Â¡tica em caso de perda de conexÃƒÆ’Ã‚Â£o.
- Compatibilidade com os principais PABXs SIP.
- Monitoramento do status de registro em tempo real.

---

## ÃƒÂ°Ã…Â¸Ã¢â‚¬Å“Ã…Â¾ Chamadas

- RealizaÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o de chamadas.
- Recebimento de chamadas.
- Encerramento de chamadas.
- Chamada em espera (Hold).
- TransferÃƒÆ’Ã‚Âªncia assistida.
- Envio de DTMF durante a chamada.
- Atendimento automÃƒÆ’Ã‚Â¡tico (Auto Answer).
- Modo NÃƒÆ’Ã‚Â£o Perturbe (DND).

---

## ÃƒÂ°Ã…Â¸Ã…Â½Ã‚Â§ ÃƒÆ’Ã‚Âudio

- SeleÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o do dispositivo de entrada (microfone).
- SeleÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o do dispositivo de saÃƒÆ’Ã‚Â­da (alto-falantes e headsets).
- Controle de volume.
- Silenciar microfone (Mute).
- Suporte para headsets USB.

---

## ÃƒÂ°Ã…Â¸Ã…Â½Ã¢â€žÂ¢ÃƒÂ¯Ã‚Â¸Ã‚Â GravaÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o de Chamadas

- GravaÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o automÃƒÆ’Ã‚Â¡tica ou manual das chamadas.
- ConfiguraÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o da pasta de gravaÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o.
- Arquivos identificados automaticamente com:
  - NÃƒÆ’Ã‚Âºmero do telefone.
  - Data.
  - Hora.
- ConfiguraÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Âµes persistidas automaticamente.

---

## ÃƒÂ°Ã…Â¸Ã¢â‚¬Å“Ã…Â  Monitoramento em Tempo Real

Durante as chamadas o sistema apresenta informaÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Âµes tÃƒÆ’Ã‚Â©cnicas como:

- Tempo da chamada.
- Codec utilizado.
- Bitrate.
- RTT (Round Trip Time).
- Jitter.
- Perda de pacotes.
- MOS estimado.
- ClassificaÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o da qualidade da chamada.

---

## ÃƒÂ°Ã…Â¸Ã…Â½Ã…Â¡ÃƒÂ¯Ã‚Â¸Ã‚Â Gerenciamento de Codecs

- Lista completa de codecs suportados.
- AtivaÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o e desativaÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o individual.
- ReordenaÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o por prioridade atravÃƒÆ’Ã‚Â©s de Drag & Drop.
- AplicaÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o automÃƒÆ’Ã‚Â¡tica das prioridades ao PJSIP.
- Salvamento automÃƒÆ’Ã‚Â¡tico das preferÃƒÆ’Ã‚Âªncias.

---

## ÃƒÂ¢Ã…Â¡Ã¢â€žÂ¢ÃƒÂ¯Ã‚Â¸Ã‚Â ConfiguraÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Âµes

O sistema permite configurar:

- Nome de exibiÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o.
- Servidor SIP.
- Ramal.
- Senha.
- Porta.
- Transporte SIP.
- Dispositivos de ÃƒÆ’Ã‚Â¡udio.
- GravaÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o de chamadas.
- Codecs.
- PreferÃƒÆ’Ã‚Âªncias gerais.

---

## ÃƒÂ°Ã…Â¸Ã¢â‚¬â€œÃ‚Â¥ÃƒÂ¯Ã‚Â¸Ã‚Â Interface

- Interface moderna desenvolvida em Flutter.
- Otimizada para Windows.
- Layout compacto.
- Componentes responsivos.
- NavegaÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o simples e intuitiva.
- ConfiguraÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Âµes organizadas por categorias.

---

## ÃƒÂ°Ã…Â¸Ã¢â‚¬ÂÃ¢â‚¬Å¾ AtualizaÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Âµes

- Estrutura preparada para atualizaÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o automÃƒÆ’Ã‚Â¡tica.
- VerificaÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o de novas versÃƒÆ’Ã‚Âµes.
- Processo simplificado de atualizaÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o.

---

## ÃƒÂ°Ã…Â¸Ã¢â‚¬ÂºÃ‚Â ÃƒÂ¯Ã‚Â¸Ã‚Â Plataforma

- Microsoft Windows.
- Interface desenvolvida em Flutter.
- Motor SIP baseado em PJSIP.
- IntegraÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o nativa com Opus.
- IntegraÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o nativa com bcg729.
- Alto desempenho utilizando bibliotecas nativas.

---

## ÃƒÂ°Ã…Â¸Ã¢â‚¬ÂÃ¢â‚¬â„¢ Estabilidade

- ReconexÃƒÆ’Ã‚Â£o automÃƒÆ’Ã‚Â¡tica da conta SIP.
- PersistÃƒÆ’Ã‚Âªncia automÃƒÆ’Ã‚Â¡tica das configuraÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Âµes.
- Tratamento de exceÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Âµes.
- Melhorias na estabilidade da interface.
- CorreÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Âµes no sistema de reordenaÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o de codecs.

---

# ÃƒÂ°Ã…Â¸Ã…â€™Ã…Â¸ Destaques da VersÃƒÆ’Ã‚Â£o 1.0

- Interface totalmente desenvolvida para ambiente desktop.
- IntegraÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o nativa com PJSIP.
- Painel de qualidade da chamada em tempo real.
- Sistema de gerenciamento de codecs.
- TransferÃƒÆ’Ã‚Âªncia assistida.
- Hold.
- Mute.
- DTMF.
- Auto Answer.
- NÃƒÆ’Ã‚Â£o Perturbe (DND).
- GravaÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o de chamadas.
- ConfiguraÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o avanÃƒÆ’Ã‚Â§ada de ÃƒÆ’Ã‚Â¡udio.
- Base preparada para futuras integraÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Âµes e novas funcionalidades.

---

# ÃƒÂ°Ã…Â¸Ã¢â‚¬â„¢Ã¢â€žÂ¢ Agradecimentos

A versÃƒÆ’Ã‚Â£o **1.0** marca o inÃƒÆ’Ã‚Â­cio de um projeto desenvolvido para oferecer uma soluÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Â£o de telefonia moderna, estÃƒÆ’Ã‚Â¡vel e eficiente.

Continuaremos evoluindo o Wconect VoIP com novos recursos, melhorias de desempenho e novas integraÃƒÆ’Ã‚Â§ÃƒÆ’Ã‚Âµes para proporcionar uma experiÃƒÆ’Ã‚Âªncia cada vez melhor aos usuÃƒÆ’Ã‚Â¡rios.

Obrigado por utilizar o **Wconect VoIP**!

---

**Wconect VoIP 1.0**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**ÃƒÂ¢Ã‚Â¬Ã¢â‚¬Â¡ÃƒÂ¯Ã‚Â¸Ã‚Â Baixar a versÃƒÆ’Ã‚Â£o 1.0.0:** [Wconect-VoIP_1.0.0.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.0/Wconect-VoIP_1.0.0.exe)