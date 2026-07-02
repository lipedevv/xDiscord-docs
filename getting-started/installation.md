---
icon: download
---

# Instalacao

## Requisitos

* Servidor Paper/Spigot moderno.
* Java 21 ou superior.
* `xCore.jar` instalado.
* `xDiscord.jar` instalado.
* Um bot criado no Discord Developer Portal.

## Arquivos

Coloque os jars na pasta `plugins/`:

```text
plugins/
  xCore.jar
  xDiscord.jar
```

O `xDiscord` depende obrigatoriamente de `xCore`:

```yaml
depend:
  - xCore
```

O `xCore` tambem declara compatibilidade com o nome antigo `fCore`, entao plugins antigos podem continuar funcionando enquanto voce migra.

## Primeiro start

Inicie o servidor uma vez. O plugin vai criar:

```text
plugins/xDiscord/locales/en_US/
plugins/xDiscord/locales/pt_BR/
plugins/xDiscord/data/
```

Depois configure o idioma, Discord e banco de dados.
