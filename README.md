---
icon: link
cover: ./Logo%20xDiscord.png
coverY: 0
layout:
  width: default
  cover:
    visible: true
    size: full
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# xDiscord

**xDiscord** e um plugin de vinculacao Minecraft + Discord feito para servidores Paper/Spigot modernos. Ele depende do **xCore** e centraliza verificacao de conta, bot Discord, recompensas, painel com botao/modal, console no Discord, comandos customizados, bloqueio de comandos para nao vinculados e sincronizacao de cargos.

## Recursos principais

* Vinculacao por codigo usando `/verificar` no Minecraft e `/vincular` no Discord.
* Vinculacao por painel no Discord com botao, modal e solicitacao para aceitar no Minecraft.
* GUI editavel com item de vincular, item de conta vinculada e confirmacao de desvinculo.
* Recompensas em modo automatico ou manual por item na GUI.
* SQLite e MySQL usando HikariCP.
* Sync de cargo verificado e cargos VIP por grupo LuckPerms/permissao.
* Nick automatico no Discord ao vincular.
* Bloqueio de comandos para jogadores nao vinculados.
* Comandos customizados no Discord.
* Ranking `/top` no Discord.
* Locales em `plugins/xDiscord/locales/<idioma>/`.

## Comece por aqui

* [Instalacao](getting-started/installation.md)
* [Configuracao rapida](getting-started/quickstart.md)
* [Arquivos e locales](configuration/locales.md)
* [Bot Discord](configuration/discord-bot.md)
