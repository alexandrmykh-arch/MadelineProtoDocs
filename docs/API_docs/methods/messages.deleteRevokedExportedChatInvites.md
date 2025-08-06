---
title: "messages.deleteRevokedExportedChatInvites"
description: "Delete all revoked chat invites"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_deleteRevokedExportedChatInvites.html
---
# Method: messages.deleteRevokedExportedChatInvites
[Back to methods index](index.html)



Delete all revoked chat invites

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|peer|[Username, chat ID, Update, Message or InputPeer](/API_docs/types/InputPeer.html) | Chat | Optional|
|admin\_id|[Username, chat ID, Update, Message or InputUser](/API_docs/types/InputUser.html) | ID of the admin that originally generated the revoked chat invites | Optional|


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

$Bool = $MadelineProto->messages->deleteRevokedExportedChatInvites(peer: $InputPeer, admin_id: $InputUser, );
```

