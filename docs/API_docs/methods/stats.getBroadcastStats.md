---
title: "stats.getBroadcastStats"
description: "Get [channel statistics](https://core.telegram.org/api/stats)"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/stats_getBroadcastStats.html
---
# Method: stats.getBroadcastStats
[Back to methods index](index.html)



Get [channel statistics](https://core.telegram.org/api/stats)

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|dark|[Bool](/API_docs/types/Bool.html) | Whether to enable dark theme for graph colors | Optional|
|channel|[Username, chat ID, Update, Message or InputChannel](/API_docs/types/InputChannel.html) | The channel | Optional|


### Return type: [stats.BroadcastStats](/API_docs/types/stats.BroadcastStats.html)

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

$stats_BroadcastStats = $MadelineProto->stats->getBroadcastStats(dark: $Bool, channel: $InputChannel, );
```

