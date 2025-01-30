---
title: "messages.getMyStickers"
description: "Fetch all [stickersets »](https://core.telegram.org/api/stickers) owned by the current user."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_getMyStickers.html
---
# Method: messages.getMyStickers
[Back to methods index](index.html)



Fetch all [stickersets »](https://core.telegram.org/api/stickers) owned by the current user.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|offset\_id|[long](/API_docs/types/long.html) | [Offsets for pagination, for more info click here](https://core.telegram.org/api/offsets) | Yes|
|limit|[int](/API_docs/types/int.html) | Maximum number of results to return, [see pagination](https://core.telegram.org/api/offsets) | Optional|


### Return type: [messages.MyStickers](/API_docs/types/messages.MyStickers.html)

### Can userbots use this method: **YES**

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$messages_MyStickers = $MadelineProto->messages->getMyStickers(offset_id: $long, limit: $int, );
```

