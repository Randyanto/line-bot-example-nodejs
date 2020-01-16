# Kitchen Sink Bot

A kitchen-sink LINE bot example

## Requirements

Install npm dependencies:

```bash
npm install
```

Also, FFmpeg and ImageMagick should be installed to test image and video
echoing.

## Configuration

Create .env file in the root folder with these variables.

```bash
CHANNEL_SECRET=YOUR_CHANNEL_SECRET
CHANNEL_ACCESS_TOKEN=YOUR_CHANNEL_ACCESS_TOKEN
BASE_URL=https://your.base.url # remove BASE_URL if you run it locally
PORT=80
```

## Run webhook server

```bash
npm start
```

With the configuration above, the webhook listens on `https://your.base.url:80/callback`.

## ngrok usage

[ngrok](https://ngrok.com/) tunnels external requests to localhost, helps
debugging local webhooks.

This example includes ngrok inside, and it just works if no `BASE_URL` is
set. Make sure that other configurations are set correctly.

```
❯ npm start

...

It seems that BASE_URL is not set. Connecting to ngrok...
listening on https://ffffffff.ngrok.io/callback
```

The URL can be directly registered as the webhook URL in LINE Developers
console.
