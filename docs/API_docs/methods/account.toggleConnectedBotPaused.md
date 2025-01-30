---
title: "account.toggleConnectedBotPaused"
description: "Pause or unpause a specific chat, temporarily disconnecting it from all [business bots »](https://core.telegram.org/api/business#connected-bots)."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/account_toggleConnectedBotPaused.html
---
# Method: account.toggleConnectedBotPaused
[Back to methods index](index.html)



Pause or unpause a specific chat, temporarily disconnecting it from all [business bots »](https://core.telegram.org/api/business#connected-bots).

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|peer|[Username, chat ID, Update, Message or InputPeer](/API_docs/types/InputPeer.html) | The chat to pause | Optional|
|paused|[Bool](/API_docs/types/Bool.html) | Whether to pause or unpause the chat | Yes|


### Return type: [Bool](/API_docs/types/Bool.html)

### Can userbots use this method: **YES**

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$Bool = $MadelineProto->account->toggleConnectedBotPaused(peer: $InputPeer, paused: $Bool, );
```

