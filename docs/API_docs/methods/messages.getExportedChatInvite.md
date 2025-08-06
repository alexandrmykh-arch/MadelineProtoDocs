---
title: "messages.getExportedChatInvite"
description: "Get info about a chat invite"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_getExportedChatInvite.html
---
# Method: messages.getExportedChatInvite
[Back to methods index](index.html)



Get info about a chat invite

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|peer|[Username, chat ID, Update, Message or InputPeer](/API_docs/types/InputPeer.html) | Chat | Optional|
|link|[string](/API_docs/types/string.html) | Invite link | Optional|


### Return type: [messages.ExportedChatInvite](/API_docs/types/messages.ExportedChatInvite.html)

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

$messages_ExportedChatInvite = $MadelineProto->messages->getExportedChatInvite(peer: $InputPeer, link: 'string', );
```

