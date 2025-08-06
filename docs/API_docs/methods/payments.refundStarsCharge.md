---
title: "payments.refundStarsCharge"
description: "Refund a [Telegram Stars](https://core.telegram.org/api/stars) transaction, see [here »](https://core.telegram.org/api/payments#6-refunds) for more info."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/payments_refundStarsCharge.html
---
# Method: payments.refundStarsCharge
[Back to methods index](index.html)



Refund a [Telegram Stars](https://core.telegram.org/api/stars) transaction, see [here »](https://core.telegram.org/api/payments#6-refunds) for more info.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|user\_id|[Username, chat ID, Update, Message or InputUser](/API_docs/types/InputUser.html) | User to refund. | Optional|
|charge\_id|[string](/API_docs/types/string.html) | Transaction ID. | Optional|


### Return type: [Updates](/API_docs/types/Updates.html)

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

$Updates = $MadelineProto->payments->refundStarsCharge(user_id: $InputUser, charge_id: 'string', );
```

