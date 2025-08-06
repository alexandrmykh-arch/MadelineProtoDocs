---
title: "channels.updatePinnedForumTopic"
description: "Pin or unpin [forum topics](https://core.telegram.org/api/forum)"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/channels_updatePinnedForumTopic.html
---
# Method: channels.updatePinnedForumTopic
[Back to methods index](index.html)



Pin or unpin [forum topics](https://core.telegram.org/api/forum)

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|channel|[Username, chat ID, Update, Message or InputChannel](/API_docs/types/InputChannel.html) | Supergroup ID | Optional|
|topic\_id|[int](/API_docs/types/int.html) | [Forum topic ID](https://core.telegram.org/api/forum) | Optional|
|pinned|[Bool](/API_docs/types/Bool.html) | Whether to pin or unpin the topic | Yes|


### Return type: [Updates](/API_docs/types/Updates.html)

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

$Updates = $MadelineProto->channels->updatePinnedForumTopic(channel: $InputChannel, topic_id: $int, pinned: $Bool, );
```

