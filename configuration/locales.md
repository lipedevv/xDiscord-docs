---
icon: language
---

# Arquivos e locales

O xDiscord separa as configuracoes por idioma.

Estrutura padrao:

```text
plugins/xDiscord/locales/en_US/config.yml
plugins/xDiscord/locales/en_US/database.yml
plugins/xDiscord/locales/en_US/discord.yml
plugins/xDiscord/locales/en_US/gui.yml
plugins/xDiscord/locales/en_US/messages.yml
plugins/xDiscord/locales/en_US/rewards.yml

plugins/xDiscord/locales/pt_BR/config.yml
plugins/xDiscord/locales/pt_BR/database.yml
plugins/xDiscord/locales/pt_BR/discord.yml
plugins/xDiscord/locales/pt_BR/gui.yml
plugins/xDiscord/locales/pt_BR/messages.yml
plugins/xDiscord/locales/pt_BR/rewards.yml
```

## Idioma ativo

O idioma ativo e lido em:

```text
plugins/xDiscord/locales/en_US/config.yml
```

```yaml
settings:
  language: "pt_BR"
```

## Atualizacao automatica

Quando uma versao nova adiciona chaves, o plugin aplica defaults automaticamente sem apagar suas configuracoes atuais.

Se alguma chave nova nao aparecer, use:

```text
/xdiscord reload
```
