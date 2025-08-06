---
title: "account.getAccountTTL"
description: "Get days to live of account"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/account_getAccountTTL.html
---
# Method: account.getAccountTTL
[Back to methods index](index.html)



Get days to live of account



### Return type: [AccountDaysTTL](/API_docs/types/AccountDaysTTL.html)

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

$AccountDaysTTL = $MadelineProto->account->getAccountTTL();
```

