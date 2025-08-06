---
title: "messages.hidePeerSettingsBar"
description: "Should be called after the user hides the [report spam/add as contact bar](https://core.telegram.org/api/action-bar) of a new chat, effectively prevents the user from executing the actions specified in the [action bar »](https://core.telegram.org/api/action-bar)."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_hidePeerSettingsBar.html
---
# Method: messages.hidePeerSettingsBar
[Back to methods index](index.html)



Should be called after the user hides the [report spam/add as contact bar](https://core.telegram.org/api/action-bar) of a new chat, effectively prevents the user from executing the actions specified in the [action bar »](https://core.telegram.org/api/action-bar).

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|peer|[Username, chat ID, Update, Message or InputPeer](/API_docs/types/InputPeer.html) | Peer | Optional|


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

$Bool = $MadelineProto->messages->hidePeerSettingsBar(peer: $InputPeer, );
```

