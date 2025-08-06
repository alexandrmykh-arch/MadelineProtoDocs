---
title: "messages.readHistory"
description: "Marks message history as read."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_readHistory.html
---
# Method: messages.readHistory
[Back to methods index](index.html)



Marks message history as read.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|peer|[Username, chat ID, Update, Message or InputPeer](/API_docs/types/InputPeer.html) | Target user or group | Optional|
|max\_id|[int](/API_docs/types/int.html) | If a positive value is passed, only messages with identifiers less or equal than the given one will be read | Optional|


### Return type: [messages.AffectedMessages](/API_docs/types/messages.AffectedMessages.html)

### Can users use this method: **YES**


### Can bots use this method: **NO**


### Can bots use this method over a business connection with the `businessConnectionId` flag: **YES**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$messages_AffectedMessages = $MadelineProto->messages->readHistory(peer: $InputPeer, max_id: $int, );
```

