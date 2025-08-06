---
title: "channels.reportAntiSpamFalsePositive"
description: "Report a [native antispam](https://core.telegram.org/api/antispam) false positive"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/channels_reportAntiSpamFalsePositive.html
---
# Method: channels.reportAntiSpamFalsePositive
[Back to methods index](index.html)



Report a [native antispam](https://core.telegram.org/api/antispam) false positive

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|channel|[Username, chat ID, Update, Message or InputChannel](/API_docs/types/InputChannel.html) | Supergroup ID | Optional|
|msg\_id|[int](/API_docs/types/int.html) | Message ID that was mistakenly deleted by the [native antispam](https://core.telegram.org/api/antispam) system, taken from the [admin log](https://core.telegram.org/api/recent-actions) | Optional|


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

$Bool = $MadelineProto->channels->reportAntiSpamFalsePositive(channel: $InputChannel, msg_id: $int, );
```

