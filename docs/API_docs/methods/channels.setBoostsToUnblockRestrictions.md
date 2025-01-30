---
title: "channels.setBoostsToUnblockRestrictions"
description: "Admins with [ban\_users admin rights »](../constructors/chatAdminRights.html) may allow users that apply a certain number of [booosts »](https://core.telegram.org/api/boost) to the group to bypass [slow mode »](../methods/channels.toggleSlowMode.html) and [other »](https://core.telegram.org/api/rights#default-rights) supergroup restrictions, see [here »](https://core.telegram.org/api/boost#bypass-slowmode-and-chat-restrictions) for more info."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/channels_setBoostsToUnblockRestrictions.html
---
# Method: channels.setBoostsToUnblockRestrictions
[Back to methods index](index.html)



Admins with [ban\_users admin rights »](../constructors/chatAdminRights.html) may allow users that apply a certain number of [booosts »](https://core.telegram.org/api/boost) to the group to bypass [slow mode »](../methods/channels.toggleSlowMode.html) and [other »](https://core.telegram.org/api/rights#default-rights) supergroup restrictions, see [here »](https://core.telegram.org/api/boost#bypass-slowmode-and-chat-restrictions) for more info.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|channel|[Username, chat ID, Update, Message or InputChannel](/API_docs/types/InputChannel.html) | The supergroup. | Optional|
|boosts|[int](/API_docs/types/int.html) | The number of required boosts (1-8, 0 to disable). | Optional|


### Return type: [Updates](/API_docs/types/Updates.html)

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

$Updates = $MadelineProto->channels->setBoostsToUnblockRestrictions(channel: $InputChannel, boosts: $int, );
```

