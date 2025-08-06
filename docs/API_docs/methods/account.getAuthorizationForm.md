---
title: "account.getAuthorizationForm"
description: "Returns a Telegram Passport authorization form for sharing data with a service"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/account_getAuthorizationForm.html
---
# Method: account.getAuthorizationForm
[Back to methods index](index.html)



Returns a Telegram Passport authorization form for sharing data with a service

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|bot\_id|[long](/API_docs/types/long.html) | User identifier of the service's bot | Yes|
|scope|[string](/API_docs/types/string.html) | Telegram Passport element types requested by the service | Optional|
|public\_key|[string](/API_docs/types/string.html) | Service's public key | Optional|


### Return type: [account.AuthorizationForm](/API_docs/types/account.AuthorizationForm.html)

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

$account_AuthorizationForm = $MadelineProto->account->getAuthorizationForm(bot_id: $long, scope: 'string', public_key: 'string', );
```

