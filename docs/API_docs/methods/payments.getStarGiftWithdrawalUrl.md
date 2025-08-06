---
title: "payments.getStarGiftWithdrawalUrl"
description: "payments.getStarGiftWithdrawalUrl parameters, return type and example"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/payments_getStarGiftWithdrawalUrl.html
---
# Method: payments.getStarGiftWithdrawalUrl
[Back to methods index](index.html)



### Parameters:

| Name     |    Type       | Required |
|----------|---------------|----------|
|stargift|[InputSavedStarGift](/API_docs/types/InputSavedStarGift.html) | Yes|
|password|[InputCheckPasswordSRP](/API_docs/types/InputCheckPasswordSRP.html) | Yes|


### Return type: [payments.StarGiftWithdrawalUrl](/API_docs/types/payments.StarGiftWithdrawalUrl.html)

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

$payments_StarGiftWithdrawalUrl = $MadelineProto->payments->getStarGiftWithdrawalUrl(stargift: $InputSavedStarGift, password: $InputCheckPasswordSRP, );
```

