---
title: "messages.checkChatInvite"
description: "Check the validity of a chat invite link and get basic info about it"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_checkChatInvite.html
---
# Method: messages.checkChatInvite
[Back to methods index](index.html)



Check the validity of a chat invite link and get basic info about it

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|hash|[string](/API_docs/types/string.html) | Invite hash from [chat invite deep link »](https://core.telegram.org/api/links#chat-invite-links). | Optional|


### Return type: [ChatInvite](/API_docs/types/ChatInvite.html)

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

$ChatInvite = $MadelineProto->messages->checkChatInvite(hash: 'string', );
```

