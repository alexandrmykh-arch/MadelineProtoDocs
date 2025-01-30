---
title: "account.toggleSponsoredMessages"
description: "Disable or re-enable Telegram ads for the current [Premium](https://core.telegram.org/api/premium) account."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/account_toggleSponsoredMessages.html
---
# Method: account.toggleSponsoredMessages
[Back to methods index](index.html)



Disable or re-enable Telegram ads for the current [Premium](https://core.telegram.org/api/premium) account.

Useful for business owners that may want to launch and view their own Telegram ads via the [Telegram ad platform »](https://ads.telegram.org).

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|enabled|[Bool](/API_docs/types/Bool.html) | Enable or disable ads. | Yes|


### Return type: [Bool](/API_docs/types/Bool.html)

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

$Bool = $MadelineProto->account->toggleSponsoredMessages(enabled: $Bool, );
```

