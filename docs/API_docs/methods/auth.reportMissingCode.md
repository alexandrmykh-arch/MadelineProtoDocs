---
title: "auth.reportMissingCode"
description: "Official apps only, reports that the SMS authentication code wasn't delivered."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/auth_reportMissingCode.html
---
# Method: auth.reportMissingCode
[Back to methods index](index.html)



Official apps only, reports that the SMS authentication code wasn't delivered.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|phone\_number|[string](/API_docs/types/string.html) | Phone number where we were supposed to receive the code | Optional|
|phone\_code\_hash|[string](/API_docs/types/string.html) | The phone code hash obtained from [auth.sendCode](../methods/auth.sendCode.html) | Optional|
|mnc|[string](/API_docs/types/string.html) | [MNC](https://en.wikipedia.org/wiki/Mobile_country_code) of the current network operator. | Optional|


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

$Bool = $MadelineProto->auth->reportMissingCode(phone_number: 'string', phone_code_hash: 'string', mnc: 'string', );
```

