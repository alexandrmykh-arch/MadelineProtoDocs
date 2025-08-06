---
title: "help.getSupport"
description: "Returns the support user for the 'ask a question' feature."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/help_getSupport.html
---
# Method: help.getSupport
[Back to methods index](index.html)



Returns the support user for the "ask a question" feature.



### Return type: [help.Support](/API_docs/types/help.Support.html)

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

$help_Support = $MadelineProto->help->getSupport();
```

