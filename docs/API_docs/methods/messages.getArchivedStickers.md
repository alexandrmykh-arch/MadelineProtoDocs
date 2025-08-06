---
title: "messages.getArchivedStickers"
description: "Get all archived stickers"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_getArchivedStickers.html
---
# Method: messages.getArchivedStickers
[Back to methods index](index.html)



Get all archived stickers

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|masks|[Bool](/API_docs/types/Bool.html) | Get [mask stickers](https://core.telegram.org/api/stickers#mask-stickers) | Optional|
|emojis|[Bool](/API_docs/types/Bool.html) | Get [custom emoji stickers](https://core.telegram.org/api/custom-emoji) | Optional|
|offset\_id|[long](/API_docs/types/long.html) | [Offsets for pagination, for more info click here](https://core.telegram.org/api/offsets) | Yes|
|limit|[int](/API_docs/types/int.html) | Maximum number of results to return, [see pagination](https://core.telegram.org/api/offsets) | Optional|


### Return type: [messages.ArchivedStickers](/API_docs/types/messages.ArchivedStickers.html)

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

$messages_ArchivedStickers = $MadelineProto->messages->getArchivedStickers(masks: $Bool, emojis: $Bool, offset_id: $long, limit: $int, );
```

