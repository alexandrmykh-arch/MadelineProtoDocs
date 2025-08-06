---
title: "payments.validateRequestedInfo"
description: "Submit requested order information for validation"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/payments_validateRequestedInfo.html
---
# Method: payments.validateRequestedInfo
[Back to methods index](index.html)



Submit requested order information for validation

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|save|[Bool](/API_docs/types/Bool.html) | Save order information to re-use it for future orders | Optional|
|invoice|[InputInvoice](/API_docs/types/InputInvoice.html) | Invoice | Yes|
|info|[PaymentRequestedInfo](/API_docs/types/PaymentRequestedInfo.html) | Requested order information | Yes|


### Return type: [payments.ValidatedRequestedInfo](/API_docs/types/payments.ValidatedRequestedInfo.html)

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

$payments_ValidatedRequestedInfo = $MadelineProto->payments->validateRequestedInfo(save: $Bool, invoice: $InputInvoice, info: $PaymentRequestedInfo, );
```

