---
title: "account.getConnectedBots"
description: "List all currently connected [business bots »](https://core.telegram.org/api/business#connected-bots)"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/account_getConnectedBots.html
---
# Method: account.getConnectedBots
[Back to methods index](index.html)



List all currently connected [business bots »](https://core.telegram.org/api/business#connected-bots)



### Return type: [account.ConnectedBots](/API_docs/types/account.ConnectedBots.html)

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

$account_ConnectedBots = $MadelineProto->account->getConnectedBots();
```

