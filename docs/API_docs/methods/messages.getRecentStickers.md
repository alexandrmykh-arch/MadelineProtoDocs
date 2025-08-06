---
title: "messages.getRecentStickers"
description: "Get recent stickers"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_getRecentStickers.html
---
# Method: messages.getRecentStickers
[Back to methods index](index.html)



Get recent stickers

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|attached|[Bool](/API_docs/types/Bool.html) | Get stickers recently attached to photo or video files | Optional|
|hash|Array of [long\|string](/API_docs/types/long\|string.html) | [Hash used for caching, for more info click here](https://core.telegram.org/api/offsets#hash-generation). | Optional|


### Return type: [messages.RecentStickers](/API_docs/types/messages.RecentStickers.html)

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

$messages_RecentStickers = $MadelineProto->messages->getRecentStickers(attached: $Bool, hash: [$long\|string, $long\|string], );
```

