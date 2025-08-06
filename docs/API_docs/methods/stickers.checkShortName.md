---
title: "stickers.checkShortName"
description: "Check whether the given short name is available"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/stickers_checkShortName.html
---
# Method: stickers.checkShortName
[Back to methods index](index.html)



Check whether the given short name is available

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|short\_name|[string](/API_docs/types/string.html) | Short name | Optional|


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

$Bool = $MadelineProto->stickers->checkShortName(short_name: 'string', );
```

