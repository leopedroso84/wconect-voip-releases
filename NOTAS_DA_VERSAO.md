# Notas da VersÃ£o â€” Wconect VoIP 1.0.1

## ðŸ”§ CorreÃ§Ãµes e melhorias

VersÃ£o de manutenÃ§Ã£o sobre a base **1.0**, focada em corrigir o
controle de volume do DTMF e em melhorar a experiÃªncia do popup de
chamada recebida em ambientes com mÃºltiplos monitores.

---

## ðŸŽšï¸ Volumes

- Corrigida a ordem de aplicaÃ§Ã£o do ganho na porta de DTMF/teste de
  alto-falante (agora alinhada ao mesmo padrÃ£o jÃ¡ usado por Toque e
  Ringback), eliminando a inconsistÃªncia encontrada numa auditoria
  completa dos 4 controles de volume (Toque, Ringback, Chamada, DTMF).

---

## ðŸ“ž Chamada recebida

- O popup de chamada recebida agora abre sempre **centralizado no mesmo
  monitor** em que a janela principal estÃ¡, mesmo em configuraÃ§Ãµes
  multi-monitor.
- Adicionado o logotipo oficial do Wconect no topo do popup.

---

## ðŸ› ï¸ Infraestrutura interna

- Adicionada instrumentaÃ§Ã£o permanente de diagnÃ³stico do pipeline de
  Ã¡udio nativo (PJSIP), ativa somente em builds de desenvolvimento â€”
  sem nenhum impacto na versÃ£o instalada pelos usuÃ¡rios.

---

**Wconect VoIP 1.0.1**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**â¬‡ï¸ Baixar a versÃ£o 1.0.1:** [Wconect-VoIP_1.0.1.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.1/Wconect-VoIP_1.0.1.exe)

---

# Notas da VersÃƒÂ£o Ã¢â‚¬â€ Wconect VoIP 1.0

## Ã°Å¸Å¡â‚¬ Bem-vindo ao Wconect VoIP 1.0

Ãƒâ€° com grande satisfaÃƒÂ§ÃƒÂ£o que apresentamos a primeira versÃƒÂ£o oficial do **Wconect VoIP**, um softphone desenvolvido para oferecer uma experiÃƒÂªncia moderna, rÃƒÂ¡pida, segura e intuitiva para comunicaÃƒÂ§ÃƒÂ£o corporativa.

Desenvolvido com Flutter e utilizando o PJSIP como motor SIP nativo, o Wconect VoIP foi projetado para oferecer alta qualidade nas chamadas, excelente desempenho e uma base sÃƒÂ³lida para futuras evoluÃƒÂ§ÃƒÂµes.

---

# Ã¢Å“Â¨ Novidades da VersÃƒÂ£o 1.0

## Ã¢ËœÅ½Ã¯Â¸Â Telefonia SIP

- Cadastro de contas SIP.
- Registro automÃƒÂ¡tico no servidor.
- ReconexÃƒÂ£o automÃƒÂ¡tica em caso de perda de conexÃƒÂ£o.
- Compatibilidade com os principais PABXs SIP.
- Monitoramento do status de registro em tempo real.

---

## Ã°Å¸â€œÅ¾ Chamadas

- RealizaÃƒÂ§ÃƒÂ£o de chamadas.
- Recebimento de chamadas.
- Encerramento de chamadas.
- Chamada em espera (Hold).
- TransferÃƒÂªncia assistida.
- Envio de DTMF durante a chamada.
- Atendimento automÃƒÂ¡tico (Auto Answer).
- Modo NÃƒÂ£o Perturbe (DND).

---

## Ã°Å¸Å½Â§ ÃƒÂudio

- SeleÃƒÂ§ÃƒÂ£o do dispositivo de entrada (microfone).
- SeleÃƒÂ§ÃƒÂ£o do dispositivo de saÃƒÂ­da (alto-falantes e headsets).
- Controle de volume.
- Silenciar microfone (Mute).
- Suporte para headsets USB.

---

## Ã°Å¸Å½â„¢Ã¯Â¸Â GravaÃƒÂ§ÃƒÂ£o de Chamadas

- GravaÃƒÂ§ÃƒÂ£o automÃƒÂ¡tica ou manual das chamadas.
- ConfiguraÃƒÂ§ÃƒÂ£o da pasta de gravaÃƒÂ§ÃƒÂ£o.
- Arquivos identificados automaticamente com:
  - NÃƒÂºmero do telefone.
  - Data.
  - Hora.
- ConfiguraÃƒÂ§ÃƒÂµes persistidas automaticamente.

---

## Ã°Å¸â€œÅ  Monitoramento em Tempo Real

Durante as chamadas o sistema apresenta informaÃƒÂ§ÃƒÂµes tÃƒÂ©cnicas como:

- Tempo da chamada.
- Codec utilizado.
- Bitrate.
- RTT (Round Trip Time).
- Jitter.
- Perda de pacotes.
- MOS estimado.
- ClassificaÃƒÂ§ÃƒÂ£o da qualidade da chamada.

---

## Ã°Å¸Å½Å¡Ã¯Â¸Â Gerenciamento de Codecs

- Lista completa de codecs suportados.
- AtivaÃƒÂ§ÃƒÂ£o e desativaÃƒÂ§ÃƒÂ£o individual.
- ReordenaÃƒÂ§ÃƒÂ£o por prioridade atravÃƒÂ©s de Drag & Drop.
- AplicaÃƒÂ§ÃƒÂ£o automÃƒÂ¡tica das prioridades ao PJSIP.
- Salvamento automÃƒÂ¡tico das preferÃƒÂªncias.

---

## Ã¢Å¡â„¢Ã¯Â¸Â ConfiguraÃƒÂ§ÃƒÂµes

O sistema permite configurar:

- Nome de exibiÃƒÂ§ÃƒÂ£o.
- Servidor SIP.
- Ramal.
- Senha.
- Porta.
- Transporte SIP.
- Dispositivos de ÃƒÂ¡udio.
- GravaÃƒÂ§ÃƒÂ£o de chamadas.
- Codecs.
- PreferÃƒÂªncias gerais.

---

## Ã°Å¸â€“Â¥Ã¯Â¸Â Interface

- Interface moderna desenvolvida em Flutter.
- Otimizada para Windows.
- Layout compacto.
- Componentes responsivos.
- NavegaÃƒÂ§ÃƒÂ£o simples e intuitiva.
- ConfiguraÃƒÂ§ÃƒÂµes organizadas por categorias.

---

## Ã°Å¸â€â€ž AtualizaÃƒÂ§ÃƒÂµes

- Estrutura preparada para atualizaÃƒÂ§ÃƒÂ£o automÃƒÂ¡tica.
- VerificaÃƒÂ§ÃƒÂ£o de novas versÃƒÂµes.
- Processo simplificado de atualizaÃƒÂ§ÃƒÂ£o.

---

## Ã°Å¸â€ºÂ Ã¯Â¸Â Plataforma

- Microsoft Windows.
- Interface desenvolvida em Flutter.
- Motor SIP baseado em PJSIP.
- IntegraÃƒÂ§ÃƒÂ£o nativa com Opus.
- IntegraÃƒÂ§ÃƒÂ£o nativa com bcg729.
- Alto desempenho utilizando bibliotecas nativas.

---

## Ã°Å¸â€â€™ Estabilidade

- ReconexÃƒÂ£o automÃƒÂ¡tica da conta SIP.
- PersistÃƒÂªncia automÃƒÂ¡tica das configuraÃƒÂ§ÃƒÂµes.
- Tratamento de exceÃƒÂ§ÃƒÂµes.
- Melhorias na estabilidade da interface.
- CorreÃƒÂ§ÃƒÂµes no sistema de reordenaÃƒÂ§ÃƒÂ£o de codecs.

---

# Ã°Å¸Å’Å¸ Destaques da VersÃƒÂ£o 1.0

- Interface totalmente desenvolvida para ambiente desktop.
- IntegraÃƒÂ§ÃƒÂ£o nativa com PJSIP.
- Painel de qualidade da chamada em tempo real.
- Sistema de gerenciamento de codecs.
- TransferÃƒÂªncia assistida.
- Hold.
- Mute.
- DTMF.
- Auto Answer.
- NÃƒÂ£o Perturbe (DND).
- GravaÃƒÂ§ÃƒÂ£o de chamadas.
- ConfiguraÃƒÂ§ÃƒÂ£o avanÃƒÂ§ada de ÃƒÂ¡udio.
- Base preparada para futuras integraÃƒÂ§ÃƒÂµes e novas funcionalidades.

---

# Ã°Å¸â€™â„¢ Agradecimentos

A versÃƒÂ£o **1.0** marca o inÃƒÂ­cio de um projeto desenvolvido para oferecer uma soluÃƒÂ§ÃƒÂ£o de telefonia moderna, estÃƒÂ¡vel e eficiente.

Continuaremos evoluindo o Wconect VoIP com novos recursos, melhorias de desempenho e novas integraÃƒÂ§ÃƒÂµes para proporcionar uma experiÃƒÂªncia cada vez melhor aos usuÃƒÂ¡rios.

Obrigado por utilizar o **Wconect VoIP**!

---

**Wconect VoIP 1.0**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**Ã¢Â¬â€¡Ã¯Â¸Â Baixar a versÃƒÂ£o 1.0.0:** [Wconect-VoIP_1.0.0.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.0/Wconect-VoIP_1.0.0.exe)