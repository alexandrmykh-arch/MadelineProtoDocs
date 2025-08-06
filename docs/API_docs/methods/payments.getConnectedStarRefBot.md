---
title: "payments.getConnectedStarRefBot"
description: "Fetch info about a specific [bot affiliation »](https://core.telegram.org/api/bots/referrals)"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/payments_getConnectedStarRefBot.html
---
# Method: payments.getConnectedStarRefBot
[Back to methods index](index.html)



Fetch info about a specific [bot affiliation »](https://core.telegram.org/api/bots/referrals)

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|peer|[Username, chat ID, Update, Message or InputPeer](/API_docs/types/InputPeer.html) | The affiliated peer | Optional|
|bot|[Username, chat ID, Update, Message or InputUser](/API_docs/types/InputUser.html) | The bot that offers the affiliate program | Optional|


### Return type: [payments.ConnectedStarRefBots](/API_docs/types/payments.ConnectedStarRefBots.html)

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

$payments_ConnectedStarRefBots = $MadelineProto->payments->getConnectedStarRefBot(peer: $InputPeer, bot: $InputUser, );
```

