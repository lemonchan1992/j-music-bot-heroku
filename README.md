# j-music-bot-heroku

Esse repositório é um guia que utiliza o [JMusicBot](https://github.com/jagrosh/MusicBot).

### Configurações iniciais (config.txt)

Para configurar o bot, é necessário colocar as informações de Discord ID do dono do bot e o Token do Discord Bot. Para isso, basta alterar os valores de BOT_TOKEN e OWNER_ID no arquivo config.txt.

Para criar um bot e gerar seu token, basta entrar na [página do discord para desenvolvedores](https://discord.com/developers/applications).

### Deploy no heroku

Para fazer o deploy no heroku, é necessário rodar os seguintes comandos na pasta desse repositório com o [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli)

#

Para fazer o login na sua conta do heroku

```bash
  heroku login
```

Para criar o app (caso já não tenha criado)

```bash
  heroku create NOME_DO_APP --no-remote
```

Para configurar o plugin java no heroku

```bash
  heroku plugins:install java
```

Por fim, fazer o deploy no heroku

```bash
  heroku deploy:jar JMusicBot-0.3.5.jar -i config.txt --app NOME_DO_APP
```
