---
title: "stories.togglePinned"
description: "Pin or unpin one or more stories"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/stories_togglePinned.html
---
# Method: stories.togglePinned
[Back to methods index](index.html)



Pin or unpin one or more stories

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|peer|[Username, chat ID, Update, Message or InputPeer](/API_docs/types/InputPeer.html) | Peer where to pin or unpin stories | Optional|
|id|Array of [int](/API_docs/types/int.html) | IDs of stories to pin or unpin | Yes|
|pinned|[Bool](/API_docs/types/Bool.html) | Whether to pin or unpin the stories | Yes|


### Return type: [Vector\_of\_int](/API_docs/types/int.html)

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

$Vector_of_int = $MadelineProto->stories->togglePinned(peer: $InputPeer, id: [$int, $int], pinned: $Bool, );
```

