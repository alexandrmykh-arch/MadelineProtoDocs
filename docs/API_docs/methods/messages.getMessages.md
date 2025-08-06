---
title: "messages.getMessages"
description: "Returns the list of messages by their IDs."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_getMessages.html
---
# Method: messages.getMessages
[Back to methods index](index.html)



# Warning: flood wait
**Warning: this method is prone to rate limiting with flood waits, **which can lead to !!! ACCOUNT BANS !!!**, please use the [updates event handler, instead (which is 100% safe) &raquo;](/docs/UPDATES.html#async-event-driven)**

# Warning: non-realtime results
**Warning: this method is not suitable for receiving messages in real-time from chats and users, please use the [updates event handler, instead &raquo;](/docs/UPDATES.html#async-event-driven)**

# Warning: this is probably NOT what you need
You probably need to use the [updates event handler, instead &raquo;](/docs/UPDATES.html#async-event-driven) :)

Returns the list of messages by their IDs.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|id|Array of [Message ID or InputMessage](/API_docs/types/InputMessage.html) | Message ID list | Yes|


### Return type: [messages.Messages](/API_docs/types/messages.Messages.html)

### Can users use this method: **YES**


### Can bots use this method: **YES**


### Can bots use this method over a business connection with the `businessConnectionId` flag: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$messages_Messages = $MadelineProto->messages->getMessages(id: [$InputMessage, $InputMessage], );
```

