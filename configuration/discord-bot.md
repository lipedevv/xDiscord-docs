---
icon: discord
---

# Bot Discord

Arquivo:

```text
plugins/xDiscord/locales/<idioma>/discord.yml
```

## Configuracao principal

```yaml
discord:
  enabled: true
  token: ""
  guild-id: ""
  invite-url: "https://discord.gg/seuservidor"
  verified-role-id: ""
  bot-status: "Use /verificar no servidor"
  command-name: "vincular"
```

## Criando o bot

1. Acesse o Discord Developer Portal.
2. Crie uma aplicacao.
3. Abra a aba Bot.
4. Crie/copiei o token.
5. Ative as intents necessarias se forem solicitadas.
6. Convide o bot com `applications.commands`.
7. Se usar cargo verificado, de permissao `Manage Roles`.

## Permissoes do bot

Para usar todos os recursos:

* `applications.commands`
* `Manage Roles`
* `Manage Nicknames`
* Permissao para ler/enviar mensagens no canal do painel.
* O cargo do bot deve estar acima dos cargos que ele vai adicionar.
