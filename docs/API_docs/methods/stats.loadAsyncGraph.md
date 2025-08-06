---
title: "stats.loadAsyncGraph"
description: "Load [channel statistics graph](https://core.telegram.org/api/stats) asynchronously"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/stats_loadAsyncGraph.html
---
# Method: stats.loadAsyncGraph
[Back to methods index](index.html)



Load [channel statistics graph](https://core.telegram.org/api/stats) asynchronously

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|token|[string](/API_docs/types/string.html) | Graph token from [statsGraphAsync](../constructors/statsGraphAsync.html) constructor | Optional|
|x|[long](/API_docs/types/long.html) | Zoom value, if required | Optional|


### Return type: [StatsGraph](/API_docs/types/StatsGraph.html)

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

$StatsGraph = $MadelineProto->stats->loadAsyncGraph(token: 'string', x: $long, );
```

