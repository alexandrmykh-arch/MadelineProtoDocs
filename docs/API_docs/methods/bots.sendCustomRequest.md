---
title: "bots.sendCustomRequest"
description: "Sends a custom request; for bots only"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/bots_sendCustomRequest.html
---
# Method: bots.sendCustomRequest
[Back to methods index](index.html)



Sends a custom request; for bots only

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|custom\_method|[string](/API_docs/types/string.html) | The method name | Optional|
|params|[DataJSON](/API_docs/types/DataJSON.html) | JSON-serialized method parameters | Yes|


### Return type: [DataJSON](/API_docs/types/DataJSON.html)

### Can users use this method: **NO**


### Can bots use this method: **YES**


### Can bots use this method over a business connection with the `businessConnectionId` flag: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$DataJSON = $MadelineProto->bots->sendCustomRequest(custom_method: 'string', params: $DataJSON, );
```

