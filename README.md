# Faris IT — WhatsApp Group Bot

ئەم بۆتە بە **Baileys / WhatsApp Web** کار دەکات و پەیام لە API ـەکەوە ڕاستەوخۆ بۆ گروپ دەدات.

> ئاگاداری: ئەمە API ـی نافەرمییە. بەکارهێنانی بۆتی WhatsApp دەتوانێت ببێتە هۆی logout یان بلۆککردنی هەژمارەکە. هەژمارەیەکی تایبەت بۆ بۆت بەکاربهێنە.

## دامەزراندن

```bash
pnpm install
cp .env.example .env
pnpm start
```

لە terminal ـەکەدا QR دەردەکەوێت. لە واتساپ:

**Settings → Linked devices → Link a device**

پاش scan ـکردنی QR، دۆخی بۆت دەبێتە `connected`.

## API

```bash
curl http://localhost:3001/health

curl -X POST http://localhost:3001/send-to-group \
  -H 'Content-Type: application/json' \
  -H 'x-api-key: change-this-key' \
  -d '{"message":"سلاڤ، ئەمە پەیامەکەی Faris IT ـە."}'
```

بۆ ناردنی خۆکار، وێبسایتەکەت دەبێت `POST /send-to-group` بانگ بکات. بۆ بەکارهێنانی دەرەکی، بۆت پێویستی بە سێرڤەرێکی هەمیشە چالاک و HTTPS هەیە.

## سێرڤەر و QR

فایلی `auth_info_baileys/` دوای scan دروست دەبێت؛ ئەمە session ـی تایبەتییە و **مەینێرە** بۆ کەسێک و **مەخە** ناو Git.
