---
title: "account.updateNotifySettings"
description: "Edits notification settings from a given user/group, from all users/all groups."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/account_updateNotifySettings.html
---
# Method: account.updateNotifySettings
[Back to methods index](index.html)



Edits notification settings from a given user/group, from all users/all groups.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|peer|[InputNotifyPeer](/API_docs/types/InputNotifyPeer.html) | Notification source | Yes|
|settings|[InputPeerNotifySettings](/API_docs/types/InputPeerNotifySettings.html) | Notification settings | Yes|


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

$Bool = $MadelineProto->account->updateNotifySettings(peer: $InputNotifyPeer, settings: $InputPeerNotifySettings, );
```

