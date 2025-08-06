---
title: "messages.sendVote"
description: "Vote in a [poll](../constructors/poll.html)"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_sendVote.html
---
# Method: messages.sendVote
[Back to methods index](index.html)



Vote in a [poll](../constructors/poll.html)

Starting from layer 159, the vote will be sent from the peer specified using [messages.saveDefaultSendAs](../methods/messages.saveDefaultSendAs.html).

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|peer|[Username, chat ID, Update, Message or InputPeer](/API_docs/types/InputPeer.html) | The chat where the poll was sent | Optional|
|msg\_id|[int](/API_docs/types/int.html) | The message ID of the poll | Optional|
|options|Array of [bytes](/API_docs/types/bytes.html) | The options that were chosen | Yes|


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

$Updates = $MadelineProto->messages->sendVote(peer: $InputPeer, msg_id: $int, options: ['bytes', 'bytes'], );
```

