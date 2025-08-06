---
title: "account.getWebAuthorizations"
description: "Get web [login widget](https://core.telegram.org/widgets/login) authorizations"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/account_getWebAuthorizations.html
---
# Method: account.getWebAuthorizations
[Back to methods index](index.html)



Get web [login widget](https://core.telegram.org/widgets/login) authorizations



### Return type: [account.WebAuthorizations](/API_docs/types/account.WebAuthorizations.html)

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

$account_WebAuthorizations = $MadelineProto->account->getWebAuthorizations();
```

