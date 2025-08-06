---
title: "payments.getStarsRevenueAdsAccountUrl"
description: "Returns a URL for a Telegram Ad platform account that can be used to set up advertisements for channel/bot in `peer`, paid using the Telegram Stars owned by the specified `peer`, see [here »](https://core.telegram.org/api/stars#paying-for-ads) for more info."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/payments_getStarsRevenueAdsAccountUrl.html
---
# Method: payments.getStarsRevenueAdsAccountUrl
[Back to methods index](index.html)



Returns a URL for a Telegram Ad platform account that can be used to set up advertisements for channel/bot in `peer`, paid using the Telegram Stars owned by the specified `peer`, see [here »](https://core.telegram.org/api/stars#paying-for-ads) for more info.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|peer|[Username, chat ID, Update, Message or InputPeer](/API_docs/types/InputPeer.html) | Channel or bot that owns the stars. | Optional|


### Return type: [payments.StarsRevenueAdsAccountUrl](/API_docs/types/payments.StarsRevenueAdsAccountUrl.html)

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

$payments_StarsRevenueAdsAccountUrl = $MadelineProto->payments->getStarsRevenueAdsAccountUrl(peer: $InputPeer, );
```

