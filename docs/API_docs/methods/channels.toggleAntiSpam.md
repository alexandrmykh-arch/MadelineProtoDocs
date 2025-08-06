---
title: "channels.toggleAntiSpam"
description: "Enable or disable the [native antispam system](https://core.telegram.org/api/antispam)."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/channels_toggleAntiSpam.html
---
# Method: channels.toggleAntiSpam
[Back to methods index](index.html)



Enable or disable the [native antispam system](https://core.telegram.org/api/antispam).

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|channel|[Username, chat ID, Update, Message or InputChannel](/API_docs/types/InputChannel.html) | Supergroup ID. The specified supergroup must have at least `telegram_antispam_group_size_min` members to enable antispam functionality, as specified by the [client configuration parameters](https://core.telegram.org/api/config#client-configuration). | Optional|
|enabled|[Bool](/API_docs/types/Bool.html) | Enable or disable the native antispam system. | Yes|


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

$Updates = $MadelineProto->channels->toggleAntiSpam(channel: $InputChannel, enabled: $Bool, );
```

