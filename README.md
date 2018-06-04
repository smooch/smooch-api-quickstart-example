# Smooch API Examples

## Get started

For a detailed guide, see the [Smooch API Quickstart](https://docs.smooch.io/guide/api-quickstart) and [our API QuickStart video tutorial](https://vimeo.com/198071401):

<a href="https://vimeo.com/198071401" target="_blank"><img src="https://i.vimeocdn.com/video/610957143.webp?mw=1800&mh=1013&q=70"
alt="VIMEO" width="240" border="10" /></a>

### Node.js

1. Clone the repository
2. Go to the _/nodejs_ subdirectory
3. Update index.js to include your secret key and key ID from your [Smooch](https://app.smooch.io) settings
4. Install dependencies (`npm install`)
5. Run the server (`node index`)
6. Use [ngrok](https://ngrok.com/) to create a secure tunnel to port 8000(`ngrok http 8000` after ngrok is installed on your PC)
7. Create a Facebook page and [connect it to Smooch](https://app.smooch.io/integrations/messenger)
8. Create a Webhook from your [dashboard](https://app.smooch.io/integrations/webhook) and point it at the full url for the /messages endpoint (e.g. https://MY-NGROK-DOMAIN.ngrok.io/messages )
9. Send messages to your Facebook page and watch the auto-replies roll in

### Scala

Go to _/scala_ subdirectory.

Get a userId from your application and change

```
# Main.scala
val userId = "aaaabbbb11112222ccccdddd"
```

Setup your app keyId and secret here
```
# application.conf
smooch {
  keyId = "app_aaaa1111bbbb3333cccc5555"
  secret = "AAAA0000BBBB1111ccccDDDD"
}
```

To run the webhook microservice, just do
```
$ sbt run
```

### Python

1. Clone the repository
2. Go to the _python_ subdirectory
3. Update main.py to include your secret key and key ID from your [Smooch](https://app.smooch.io) settings
4. Install dependencies (`pip install -r requirements.txt`)
5. Run the server (`FLASK_APP=main.py flask run`)
6. Use [ngrok](https://ngrok.com/) to create a secure tunnel to port 5000(`ngrok http 5000` after ngrok is installed on your PC)
7. Create a Facebook page and [connect it to Smooch](https://app.smooch.io/integrations/messenger)
8. Create a Webhook from your [dashboard](https://app.smooch.io/integrations/webhook) and point it at the full url for the /messages endpoint (e.g. https://MY-NGROK-DOMAIN.ngrok.io/messages )
9. Send messages to your Facebook page and watch the auto-replies roll in
