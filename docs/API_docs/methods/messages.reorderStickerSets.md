---
title: "messages.reorderStickerSets"
description: "Reorder installed stickersets"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_reorderStickerSets.html
---
# Method: messages.reorderStickerSets
[Back to methods index](index.html)



Reorder installed stickersets

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|masks|[Bool](/API_docs/types/Bool.html) | Reorder mask stickersets | Optional|
|emojis|[Bool](/API_docs/types/Bool.html) | Reorder [custom emoji stickersets](https://core.telegram.org/api/custom-emoji) | Optional|
|order|Array of [long](/API_docs/types/long.html) | New stickerset order by stickerset IDs | Yes|


### Return type: [Bool](/API_docs/types/Bool.html)

### Can users use this method: **YES**


### Can bots use this method: **NO**


### Can bots use this method over a business connection with the `businessConnectionId` flag: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$Bool = $MadelineProto->messages->reorderStickerSets(masks: $Bool, emojis: $Bool, order: [$long, $long], );
```

