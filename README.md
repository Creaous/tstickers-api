# Telegram Sticker API
This is basically a wrapper around the Telegram Bot API that only provides access to sticker data. It aggressively caches sticker image data both on-disk and in the `Cache-Control` header, both to save requests to Telegram and to save requests from clients.

## Features
- Public sticker API
- Automatically handles WebP -> PNG conversion
- Aggressive file caching for fast response times
- Pre-set CORS headers -- use it in client-side JS immediately

## Usage
Rename `config.example.json` to `config.json` and edit the values as required.

Then:
```shell
npm i
npm start
```

## Endpoints
### **GET** /pack/:name
Returns a sticker pack's data.

Example: `https://example.com/pack/Animals`

### **GET** /sticker/:id.png
Returns a valid sticker image.

Example: `https://example.com/sticker/CAADAgAD3gAD9HsZAAG9he9u98XOPQI.png`
