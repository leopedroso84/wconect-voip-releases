# Wconect VoIP — Releases

Este repositório contém **apenas** os instaladores publicados do
[Wconect VoIP](https://github.com/leopedroso84/wconect-sip) e o manifesto de
atualização (`latest.json`) usado pelo próprio aplicativo para verificar se
há uma versão nova disponível.

Não há código-fonte aqui — o desenvolvimento acontece em um repositório
privado separado.

## Baixando o instalador

- **Versão mais recente (link estável)**: sempre em
  [`releases/download/latest/Wconect-VoIP_Setup.exe`](https://github.com/leopedroso84/wconect-voip-releases/releases/download/latest/Wconect-VoIP_Setup.exe) —
  o nome do arquivo **nunca muda**, então esse link pode ser salvo/
  divulgado sem se preocupar com o número da versão.
- **Uma versão específica/anterior**: veja a
  [lista de releases](https://github.com/leopedroso84/wconect-voip-releases/releases) —
  cada versão publicada fica arquivada permanentemente com o instalador
  nomeado `Wconect-VoIP_X.Y.Z.exe`.

## Changelog

`CHANGELOG.txt` acumula o histórico completo de todas as versões
(mais recente no topo), no formato:

```
versão 1.0.1
----------------
1. Item novo desta versão
2. Outro item

versão 1.0.0
----------------
1. Item da versão anterior
...
```

Mesmo texto aparece no corpo de cada release do GitHub (inclusive a
"latest") - padrão inspirado no
[FxSound](https://github.com/fxsound2/fxsound-app/releases/tag/latest).
Sempre em Português do Brasil.

## `latest.json`

```json
{
  "version": "1.0.0",
  "installer_url": "https://github.com/leopedroso84/wconect-voip-releases/releases/download/latest/Wconect-VoIP_Setup.exe",
  "archive_url": "https://github.com/leopedroso84/wconect-voip-releases/releases/download/v1.0.0/Wconect-VoIP_1.0.0.exe",
  "published_at": "2026-07-26T12:00:00Z",
  "notes": "Resumo em texto simples das mudanças desta versão."
}
```

Atualizado automaticamente por `tools/publish_release.ps1` (repositório
privado) a cada nova versão publicada — ver `docs/packaging.md` lá.

## Retenção de versões antigas

Ainda não definida — a decisão fica para uma etapa futura.
