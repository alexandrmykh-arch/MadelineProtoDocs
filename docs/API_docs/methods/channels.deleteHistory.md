---
title: "channels.deleteHistory"
description: "Delete the history of a [supergroup](https://core.telegram.org/api/channel)"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/channels_deleteHistory.html
---
# Method: channels.deleteHistory
[Back to methods index](index.html)



Delete the history of a [supergroup](https://core.telegram.org/api/channel)

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|for\_everyone|[Bool](/API_docs/types/Bool.html) | Whether the history should be deleted for everyone | Optional|
|channel|[Username, chat ID, Update, Message or InputChannel](/API_docs/types/InputChannel.html) | [Supergroup](https://core.telegram.org/api/channel) whose history must be deleted | Optional|
|max\_id|[int](/API_docs/types/int.html) | ID of message **up to which** the history must be deleted | Optional|


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

$Updates = $MadelineProto->channels->deleteHistory(for_everyone: $Bool, channel: $InputChannel, max_id: $int, );
```

