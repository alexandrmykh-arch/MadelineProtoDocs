---
title: "channels.editBanned"
description: "Ban/unban/kick a user in a [supergroup/channel](https://core.telegram.org/api/channel)."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/channels_editBanned.html
---
# Method: channels.editBanned
[Back to methods index](index.html)



Ban/unban/kick a user in a [supergroup/channel](https://core.telegram.org/api/channel).

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|channel|[Username, chat ID, Update, Message or InputChannel](/API_docs/types/InputChannel.html) | The [supergroup/channel](https://core.telegram.org/api/channel). | Optional|
|participant|[Username, chat ID, Update, Message or InputPeer](/API_docs/types/InputPeer.html) | Participant to ban | Optional|
|banned\_rights|[ChatBannedRights](/API_docs/types/ChatBannedRights.html) | The banned rights | Yes|


### Return type: [Updates](/API_docs/types/Updates.html)

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

$Updates = $MadelineProto->channels->editBanned(channel: $InputChannel, participant: $InputPeer, banned_rights: $ChatBannedRights, );
```

