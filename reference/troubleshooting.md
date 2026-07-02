---
icon: triangle-alert
---

# Problemas comuns

## xDiscord nao inicia

Confira se `xCore.jar` esta na pasta `plugins/`.

## Bot fica pensando

Verifique o token, `guild-id` e permissoes do bot. O plugin usa `deferReply` e sempre tenta finalizar a resposta, mas erro de token/guild/permissao pode impedir interacoes.

## Cargo nao e adicionado

Confira:

* `verified-role-id`
* `discord-role-id` dos VIPs
* permissao `Manage Roles`
* hierarquia dos cargos no Discord

O cargo do bot precisa estar acima dos cargos que ele vai gerenciar.

## Nick nao muda

Confira:

* `discord.nickname-sync.enabled`
* permissao `Manage Nicknames`
* hierarquia de cargos

## Painel duplica

Confira `discord.link-panel.message-id`. O xDiscord salva esse ID automaticamente. Se apagar o ID, ele tenta encontrar uma mensagem antiga do bot no canal; se nao achar, envia uma nova.

## MySQL nao conecta

Confira:

* host
* porta
* database
* usuario/senha
* firewall
* `useSSL`
