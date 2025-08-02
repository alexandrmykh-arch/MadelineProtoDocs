---
title: "stories.createAlbum"
description: "stories.createAlbum parameters, return type and example"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/stories_createAlbum.html
---
# Method: stories.createAlbum
[Back to methods index](index.html)



### Parameters:

| Name     |    Type       | Required |
|----------|---------------|----------|
|peer|[Username, chat ID, Update, Message or InputPeer](/API_docs/types/InputPeer.html) | Optional|
|title|[string](/API_docs/types/string.html) | Optional|
|stories|Array of [int](/API_docs/types/int.html) | Yes|


### Return type: [StoryAlbum](/API_docs/types/StoryAlbum.html)

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

$StoryAlbum = $MadelineProto->stories->createAlbum(peer: $InputPeer, title: 'string', stories: [$int, $int], );
```

