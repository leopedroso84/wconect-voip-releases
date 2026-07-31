# Notas da Versão — Wconect VoIP 1.0.21

## 🎧 Tela de Áudio reorganizada

- Configurações agrupadas por função: Alto-falante, Microfone e Toques
  e teclado, cada um reunindo tudo relacionado num só lugar.
- Novo controle de Volume do microfone (0-100%, independente do
  Boost) - agora dá pra reduzir o microfone direto pelo app, sem
  precisar abrir as configurações de som do Windows.

---

**Wconect VoIP 1.0.21**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**⬇️ Baixar a versão 1.0.21:** [Wconect-VoIP_1.0.21.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.21/Wconect-VoIP_1.0.21.exe)

---

# Notas da Versão — Wconect VoIP 1.0.20

## 📞 Melhorias na experiência de chamada

- O indicador visual de "em ligação" agora já modula assim que a
  chamada começa a tocar, em vez de só depois de atendida - reforça
  que a ligação está em andamento.
- Checagem automática de atualização ficou mais rápida (a cada 3
  minutos, em vez de 15).

---

**Wconect VoIP 1.0.20**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**⬇️ Baixar a versão 1.0.20:** [Wconect-VoIP_1.0.20.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.20/Wconect-VoIP_1.0.20.exe)

---

# Notas da Versão — Wconect VoIP 1.0.19

## 📊 Investigação de quedas de chamada

- Cada chamada agora recebe um identificador único, registrado do início
  ao fim - facilita cruzar o log com o histórico de chamadas.
- Ao encerrar, o log registra ramal, destino, duração, código SIP e a
  origem do encerramento (você desligou, o destino recusou/estava
  ocupado, o PABX encerrou, ou o outro lado desligou) - base para
  identificar com precisão a causa de quedas de chamada relatadas.

## 🩺 Instrumentação permanente

- Eventos de minimizar, restaurar, maximizar e foco da janela principal
  agora ficam registrados no log (antes não deixavam nenhum rastro).
- Eventos do headset (tirar do gancho, mudo, espera) agora são
  registrados também em produção, não só em builds de desenvolvimento.
- Cada linha do log agora identifica de qual janela/processo interno
  ela veio, facilitando reconstruir a sequência de eventos de um
  travamento relatado.

---

**Wconect VoIP 1.0.19**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**⬇️ Baixar a versão 1.0.19:** [Wconect-VoIP_1.0.19.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.19/Wconect-VoIP_1.0.19.exe)

---

# Notas da Versão — Wconect VoIP 1.0.18

## 🛠️ Estabilidade (causa raiz do travamento da bandeja)

Analisamos ao vivo um crash real (log de eventos do Windows + dump completo de
memória) e identificamos duas causas concretas de corrupção de memória:

- **`screen_retriever` (detecção de monitor)**: o código nativo não checava
  se a chamada ao Windows para obter informações do monitor tinha sucesso.
  Quando falhava (situação real, ligada a mudanças no estado dos monitores),
  o app seguia usando dados de memória não inicializados como se fossem
  válidos - uma causa direta de corrupção de memória. Corrigido.
- **Comunicação entre janelas** (popup de chamada recebida, janela de
  atualização, janela "Sobre"): uma desreferência de ponteiro nulo não
  verificada foi corrigida no mecanismo usado por toda essa comunicação.

Essas duas correções foram encontradas ao analisar um dump de memória real de
um travamento capturado em produção - não são apenas hipóteses.

## ☎️ Discagem de códigos do PABX

- Corrigido um bug real que impedia discar códigos de facilidade do PABX
  (transferência, estacionamento, captura de ligação, correio de voz, etc. -
  ex.: `*2`, `#2`, `*8`, `*21`, `*68` + ramal, `*0*`). Esses códigos agora são
  discados normalmente, a qualquer momento, sem passar pela validação de
  número de telefone.

## 📞 Ligação ativa

- A janela principal agora permanece sempre em primeiro plano enquanto
  houver uma ligação ativa, mesmo navegando em outras janelas/telas -
  facilita monitorar e usar espera/mudo sem perder a ligação de vista.
  Volta ao comportamento normal assim que a ligação termina.

## 🩺 Diagnóstico HID

- Corrigida quebra de texto letra-por-letra no painel de diagnóstico HID
  (modo desenvolvedor) em janela estreita.

---

**Wconect VoIP 1.0.18**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**⬇️ Baixar a versão 1.0.18:** [Wconect-VoIP_1.0.18.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.18/Wconect-VoIP_1.0.18.exe)

---

# Notas da Versão — Wconect VoIP 1.0.17

## 📞 Chamada recebida

- Botões invertidos: **Atender** agora fica à esquerda e **Recusar** à direita,
  reduzindo erro de operação ao atender rápido.

## ☎️ Discagem

- Números digitados, colados ou vindos de Recentes/Contatos agora são
  normalizados automaticamente para o padrão que o PABX espera, aceitando
  qualquer formatação (espaços, parênteses, hífen, ponto, "+55"/"55"/"0055").
  Números inválidos são bloqueados com um aviso claro em vez de simplesmente
  não discar.

## 🔔 Fim de chamada

- Um bipe curto agora toca sempre que uma chamada termina de verdade
  (você desliga, o outro lado desliga, o PABX encerra, ou uma transferência
  assistida é concluída) - nunca ao iniciar ou durante uma transferência.

## 🛠️ Estabilidade

- Corrigido vazamento de recursos (ícone/menu) da bandeja do sistema e um
  bug conhecido em que o menu de contexto às vezes não fechava direito.
- Reforçada a proteção contra travamentos: callbacks da bandeja e do
  headset agora nunca derrubam o aplicativo, mesmo em caso de erro
  inesperado.
- Corrigida a quebra de texto letra-por-letra no painel de diagnóstico
  HID (modo desenvolvedor) em janela estreita.

---

**Wconect VoIP 1.0.17**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**⬇️ Baixar a versão 1.0.17:** [Wconect-VoIP_1.0.17.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.17/Wconect-VoIP_1.0.17.exe)

---

# Notas da Versão — Wconect VoIP 1.0.16

## 🔄 Correção da atualização automática

- Corrigido um problema que podia exibir o aviso de atualização novamente
  mesmo depois de o app já estar atualizado. Após instalar esta versão,
  o aviso só aparecerá quando houver uma versão realmente mais nova.

---

**Wconect VoIP 1.0.16**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**⬇️ Baixar a versão 1.0.16:** [Wconect-VoIP_1.0.16.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.16/Wconect-VoIP_1.0.16.exe)

---

# Notas da Versão — Wconect VoIP 1.0.15

## 📞 Ramais internos no formato correto

- Corrigida a identificação de chamadas recebidas de ramais internos.
  Ramais como `1000`, `1021`, `2000` e `5000` agora aparecem exatamente
  nesse formato no popup, sem serem confundidos com números internacionais.

---

**Wconect VoIP 1.0.15**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**⬇️ Baixar a versão 1.0.15:** [Wconect-VoIP_1.0.15.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.15/Wconect-VoIP_1.0.15.exe)

---

# Notas da Versão — Wconect VoIP 1.0.14

## 🔄 Mais um ajuste na janela de atualização

- Corrigido um caso em que a janela "Atualização disponível" podia
  aparecer desalinhada quando o aviso surgia com o app minimizado na
  bandeja.

---

**Wconect VoIP 1.0.14**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**⬇️ Baixar a versão 1.0.14:** [Wconect-VoIP_1.0.14.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.14/Wconect-VoIP_1.0.14.exe)

---

# Notas da Versão — Wconect VoIP 1.0.13

## 🔄 Janela de atualização mais confiável

- Corrigido um caso em que a janela "Atualização disponível" podia
  abrir fora do centro da janela principal, dependendo da resolução
  ou escala da tela.

---

**Wconect VoIP 1.0.13**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**⬇️ Baixar a versão 1.0.13:** [Wconect-VoIP_1.0.13.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.13/Wconect-VoIP_1.0.13.exe)

---

# Notas da Versão — Wconect VoIP 1.0.12

## 📞 Chamada recebida mais confiável

- O popup de chamada recebida agora sempre abre centralizado no
  monitor principal, mesmo com vários monitores conectados.
- Não aparece mais um breve flash branco na tela ao receber uma
  chamada.
- O número do contato é exibido formatado no padrão brasileiro
  ((DD) 9XXXX-XXXX para celular, (DD) XXXX-XXXX para fixo), sem
  sufixos internos do PABX que antes apareciam junto do número.

---

**Wconect VoIP 1.0.12**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**⬇️ Baixar a versão 1.0.12:** [Wconect-VoIP_1.0.12.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.12/Wconect-VoIP_1.0.12.exe)

---

# Notas da Versão — Wconect VoIP 1.0.11

## 📞 Popup de chamada recebida com animação

O ícone de ligação agora pulsa enquanto a chamada toca, e o rótulo
"Chamada recebida" ganhou um visual mais elegante.

---

**Wconect VoIP 1.0.11**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**⬇️ Baixar a versão 1.0.11:** [Wconect-VoIP_1.0.11.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.11/Wconect-VoIP_1.0.11.exe)

---

# Notas da Versão — Wconect VoIP 1.0.10

## 📞 Popup de chamada recebida com logo

O logotipo oficial voltou ao topo do popup de chamada recebida.

## 📇 Primeiros passos da agenda de contatos

Ao clicar num item de "Recentes", o app agora pergunta se você quer
ligar de novo ou salvar o contato (nome + telefone) - primeiro passo
para montar sua agenda a partir do histórico de chamadas.

---

**Wconect VoIP 1.0.10**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**⬇️ Baixar a versão 1.0.10:** [Wconect-VoIP_1.0.10.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.10/Wconect-VoIP_1.0.10.exe)

---

# Notas da Versão — Wconect VoIP 1.0.9

## ⚡ Aviso de atualização em segundo plano

O app agora checa por novas versões periodicamente enquanto está aberto
(a cada 15 minutos), não só ao abrir - o aviso pode aparecer minutos
depois de uma nova versão ser publicada, sem precisar fechar e abrir de
novo. Clicar em "Depois" agora é respeitado pelo resto da sessão - o
aviso só volta a aparecer na próxima vez que você abrir o app.

---

**Wconect VoIP 1.0.9**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**⬇️ Baixar a versão 1.0.9:** [Wconect-VoIP_1.0.9.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.9/Wconect-VoIP_1.0.9.exe)

---

# Notas da Versão — Wconect VoIP 1.0.7

## 🧹 Discador mais limpo

O número digitado agora limpa sozinho assim que você desliga uma
ligação e volta pro discador.

## 📋 Log de diagnóstico sempre ativo

O log interno do app agora é mais robusto: grava um arquivo por dia e
se auto-recupera caso pare de escrever por qualquer motivo - importante
pra conseguirmos investigar qualquer problema relatado.

---

**Wconect VoIP 1.0.7**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**⬇️ Baixar a versão 1.0.7:** [Wconect-VoIP_1.0.7.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.7/Wconect-VoIP_1.0.7.exe)

---

# Notas da Versão — Wconect VoIP 1.0.6

## 📞 Popup de chamada recebida mais limpo

O aviso de chamada recebida ficou mais organizado: removemos o
logotipo e o ícone que ficavam junto do texto, e centralizamos "Chamada
recebida" e o nome/número na tela.

---

**Wconect VoIP 1.0.6**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**⬇️ Baixar a versão 1.0.6:** [Wconect-VoIP_1.0.6.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.6/Wconect-VoIP_1.0.6.exe)

---

# Notas da Versão — Wconect VoIP 1.0.5

## ⚡ Aviso de atualização mais rápido

A checagem de nova versão agora detecta uma release recém-publicada
quase na hora, em vez de esperar alguns minutos pelo cache do GitHub.

---

**Wconect VoIP 1.0.5**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**⬇️ Baixar a versão 1.0.5:** [Wconect-VoIP_1.0.5.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.5/Wconect-VoIP_1.0.5.exe)

---

# Notas da Versão — Wconect VoIP 1.0.4

## 🎧 Codec Opus habilitado

O codec Opus (alta qualidade de áudio, adaptável à rede) voltou a ficar
disponível na lista de codecs suportados.

---

**Wconect VoIP 1.0.4**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**⬇️ Baixar a versão 1.0.4:** [Wconect-VoIP_1.0.4.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.4/Wconect-VoIP_1.0.4.exe)

---

# Notas da Versão — Wconect VoIP 1.0.3

## 🖥️ Aviso de atualização mais organizado

O aviso de "Atualização disponível" agora abre numa janela própria,
sempre centralizada sobre o Wconect VoIP e no monitor certo - antes o
conteúdo podia ficar espremido ou desalinhado dependendo do tamanho da
janela do app.

---

**Wconect VoIP 1.0.3**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**⬇️ Baixar a versão 1.0.3:** [Wconect-VoIP_1.0.3.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.3/Wconect-VoIP_1.0.3.exe)

---

# Notas da Versão — Wconect VoIP 1.0.2

## 🔧 Correção importante

Corrigimos um problema que podia travar o aplicativo logo ao abrir,
afetando o funcionamento correto do ícone na bandeja do sistema
(aquele ícone perto do relógio, usado para abrir ou fechar o Wconect
VoIP). Com essa correção, o app abre normalmente e o menu do ícone da
bandeja volta a funcionar como esperado.

---

## 🖥️ Diálogo "Atualização disponível"

- Visual reorganizado, mais limpo e alinhado ao restante do app.
- A lista de novidades de cada versão agora aparece bem formatada,
  item por item.

---

**Wconect VoIP 1.0.2**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**⬇️ Baixar a versão 1.0.2:** [Wconect-VoIP_1.0.2.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.2/Wconect-VoIP_1.0.2.exe)

---

# Notas da Versão — Wconect VoIP 1.0.1

## 🔧 Correções e melhorias

Versão de manutenção sobre a base **1.0**, focada em corrigir o
controle de volume do DTMF e em melhorar a experiência do popup de
chamada recebida em ambientes com múltiplos monitores.

---

## 🎚️ Volumes

- Corrigida a ordem de aplicação do ganho na porta de DTMF/teste de
  alto-falante (agora alinhada ao mesmo padrão já usado por Toque e
  Ringback), eliminando a inconsistência encontrada numa auditoria
  completa dos 4 controles de volume (Toque, Ringback, Chamada, DTMF).

---

## 📞 Chamada recebida

- O popup de chamada recebida agora abre sempre **centralizado no mesmo
  monitor** em que a janela principal está, mesmo em configurações
  multi-monitor.
- Adicionado o logotipo oficial do Wconect no topo do popup.

---

## 🛠️ Infraestrutura interna

- Adicionada instrumentação permanente de diagnóstico do pipeline de
  áudio nativo (PJSIP), ativa somente em builds de desenvolvimento —
  sem nenhum impacto na versão instalada pelos usuários.

---

**Wconect VoIP 1.0.1**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**⬇️ Baixar a versão 1.0.1:** [Wconect-VoIP_1.0.1.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.1/Wconect-VoIP_1.0.1.exe)

---

# Notas da Versão — Wconect VoIP 1.0

## 🚀 Bem-vindo ao Wconect VoIP 1.0

É com grande satisfação que apresentamos a primeira versão oficial do **Wconect VoIP**, um softphone desenvolvido para oferecer uma experiência moderna, rápida, segura e intuitiva para comunicação corporativa.

Desenvolvido com Flutter e utilizando o PJSIP como motor SIP nativo, o Wconect VoIP foi projetado para oferecer alta qualidade nas chamadas, excelente desempenho e uma base sólida para futuras evoluções.

---

# ✨ Novidades da Versão 1.0

## ☎️ Telefonia SIP

- Cadastro de contas SIP.
- Registro automático no servidor.
- Reconexão automática em caso de perda de conexão.
- Compatibilidade com os principais PABXs SIP.
- Monitoramento do status de registro em tempo real.

---

## 📞 Chamadas

- Realização de chamadas.
- Recebimento de chamadas.
- Encerramento de chamadas.
- Chamada em espera (Hold).
- Transferência assistida.
- Envio de DTMF durante a chamada.
- Atendimento automático (Auto Answer).
- Modo Não Perturbe (DND).

---

## 🎧 Áudio

- Seleção do dispositivo de entrada (microfone).
- Seleção do dispositivo de saída (alto-falantes e headsets).
- Controle de volume.
- Silenciar microfone (Mute).
- Suporte para headsets USB.

---

## 🎙️ Gravação de Chamadas

- Gravação automática ou manual das chamadas.
- Configuração da pasta de gravação.
- Arquivos identificados automaticamente com:
  - Número do telefone.
  - Data.
  - Hora.
- Configurações persistidas automaticamente.

---

## 📊 Monitoramento em Tempo Real

Durante as chamadas o sistema apresenta informações técnicas como:

- Tempo da chamada.
- Codec utilizado.
- Bitrate.
- RTT (Round Trip Time).
- Jitter.
- Perda de pacotes.
- MOS estimado.
- Classificação da qualidade da chamada.

---

## 🎚️ Gerenciamento de Codecs

- Lista completa de codecs suportados.
- Ativação e desativação individual.
- Reordenação por prioridade através de Drag & Drop.
- Aplicação automática das prioridades ao PJSIP.
- Salvamento automático das preferências.

---

## ⚙️ Configurações

O sistema permite configurar:

- Nome de exibição.
- Servidor SIP.
- Ramal.
- Senha.
- Porta.
- Transporte SIP.
- Dispositivos de áudio.
- Gravação de chamadas.
- Codecs.
- Preferências gerais.

---

## 🖥️ Interface

- Interface moderna desenvolvida em Flutter.
- Otimizada para Windows.
- Layout compacto.
- Componentes responsivos.
- Navegação simples e intuitiva.
- Configurações organizadas por categorias.

---

## 🔄 Atualizações

- Estrutura preparada para atualização automática.
- Verificação de novas versões.
- Processo simplificado de atualização.

---

## 🛠️ Plataforma

- Microsoft Windows.
- Interface desenvolvida em Flutter.
- Motor SIP baseado em PJSIP.
- Integração nativa com Opus.
- Integração nativa com bcg729.
- Alto desempenho utilizando bibliotecas nativas.

---

## 🔒 Estabilidade

- Reconexão automática da conta SIP.
- Persistência automática das configurações.
- Tratamento de exceções.
- Melhorias na estabilidade da interface.
- Correções no sistema de reordenação de codecs.

---

# 🌟 Destaques da Versão 1.0

- Interface totalmente desenvolvida para ambiente desktop.
- Integração nativa com PJSIP.
- Painel de qualidade da chamada em tempo real.
- Sistema de gerenciamento de codecs.
- Transferência assistida.
- Hold.
- Mute.
- DTMF.
- Auto Answer.
- Não Perturbe (DND).
- Gravação de chamadas.
- Configuração avançada de áudio.
- Base preparada para futuras integrações e novas funcionalidades.

---

# 💙 Agradecimentos

A versão **1.0** marca o início de um projeto desenvolvido para oferecer uma solução de telefonia moderna, estável e eficiente.

Continuaremos evoluindo o Wconect VoIP com novos recursos, melhorias de desempenho e novas integrações para proporcionar uma experiência cada vez melhor aos usuários.

Obrigado por utilizar o **Wconect VoIP**!

---

**Wconect VoIP 1.0**
*Conectando pessoas com qualidade, desempenho e simplicidade.*

**⬇️ Baixar a versão 1.0.0:** [Wconect-VoIP_1.0.0.exe](https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.0/Wconect-VoIP_1.0.0.exe)