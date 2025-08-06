---
title: "chatlists.joinChatlistInvite"
description: "Import a [chat folder deep link »](https://core.telegram.org/api/links#chat-folder-links), joining some or all the chats in the folder."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/chatlists_joinChatlistInvite.html
---
# Method: chatlists.joinChatlistInvite
[Back to methods index](index.html)



Import a [chat folder deep link »](https://core.telegram.org/api/links#chat-folder-links), joining some or all the chats in the folder.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|slug|[string](/API_docs/types/string.html) | `slug` obtained from a [chat folder deep link »](https://core.telegram.org/api/links#chat-folder-links). | Optional|
|peers|Array of [Username, chat ID, Update, Message or InputPeer](/API_docs/types/InputPeer.html) | List of new chats to join, fetched using [chatlists.checkChatlistInvite](../methods/chatlists.checkChatlistInvite.html) and filtered as specified in the [documentation »](https://core.telegram.org/api/folders#shared-folders). | Yes|


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

$Updates = $MadelineProto->chatlists->joinChatlistInvite(slug: 'string', peers: [$InputPeer, $InputPeer], );
```

