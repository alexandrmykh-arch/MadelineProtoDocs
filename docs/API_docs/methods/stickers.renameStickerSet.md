---
title: "stickers.renameStickerSet"
description: "Renames a stickerset."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/stickers_renameStickerSet.html
---
# Method: stickers.renameStickerSet
[Back to methods index](index.html)



Renames a stickerset.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|stickerset|[InputStickerSet](/API_docs/types/InputStickerSet.html) | Stickerset to rename | Optional|
|title|[string](/API_docs/types/string.html) | New stickerset title | Optional|


### Return type: [messages.StickerSet](/API_docs/types/messages.StickerSet.html)

### Can userbots use this method: **YES**

### Can bots use this method: **YES**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$messages_StickerSet = $MadelineProto->stickers->renameStickerSet(stickerset: $InputStickerSet, title: 'string', );
```

