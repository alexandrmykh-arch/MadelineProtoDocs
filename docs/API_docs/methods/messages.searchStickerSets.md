---
title: "messages.searchStickerSets"
description: "Search for stickersets"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_searchStickerSets.html
---
# Method: messages.searchStickerSets
[Back to methods index](index.html)



Search for stickersets

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|exclude\_featured|[Bool](/API_docs/types/Bool.html) | Exclude featured stickersets from results | Optional|
|q|[string](/API_docs/types/string.html) | Query string | Optional|
|hash|Array of [long\|string](/API_docs/types/long\|string.html) | [Hash used for caching, for more info click here](https://core.telegram.org/api/offsets#hash-generation). | Optional|


### Return type: [messages.FoundStickerSets](/API_docs/types/messages.FoundStickerSets.html)

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

$messages_FoundStickerSets = $MadelineProto->messages->searchStickerSets(exclude_featured: $Bool, q: 'string', hash: [$long\|string, $long\|string], );
```

