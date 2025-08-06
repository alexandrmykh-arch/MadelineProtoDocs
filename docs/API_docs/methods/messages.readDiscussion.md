---
title: "messages.readDiscussion"
description: "Mark a [thread](https://core.telegram.org/api/threads) as read"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_readDiscussion.html
---
# Method: messages.readDiscussion
[Back to methods index](index.html)



Mark a [thread](https://core.telegram.org/api/threads) as read

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|peer|[Username, chat ID, Update, Message or InputPeer](/API_docs/types/InputPeer.html) | Group ID | Optional|
|msg\_id|[int](/API_docs/types/int.html) | ID of message that started the thread | Optional|
|read\_max\_id|[int](/API_docs/types/int.html) | ID up to which thread messages were read | Optional|


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

$Bool = $MadelineProto->messages->readDiscussion(peer: $InputPeer, msg_id: $int, read_max_id: $int, );
```

