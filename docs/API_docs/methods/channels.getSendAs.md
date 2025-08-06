---
title: "channels.getSendAs"
description: "Obtains a list of peers that can be used to send messages in a specific group"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/channels_getSendAs.html
---
# Method: channels.getSendAs
[Back to methods index](index.html)



Obtains a list of peers that can be used to send messages in a specific group

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|for\_paid\_reactions|[Bool](/API_docs/types/Bool.html) |  | Optional|
|peer|[Username, chat ID, Update, Message or InputPeer](/API_docs/types/InputPeer.html) | The group where we intend to send messages | Optional|


### Return type: [channels.SendAsPeers](/API_docs/types/channels.SendAsPeers.html)

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

$channels_SendAsPeers = $MadelineProto->channels->getSendAs(for_paid_reactions: $Bool, peer: $InputPeer, );
```

