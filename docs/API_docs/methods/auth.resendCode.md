---
title: "auth.resendCode"
description: "Resend the login code via another medium, the phone code type is determined by the return value of the previous auth.sendCode/auth.resendCode: see [login](https://core.telegram.org/api/auth) for more info."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/auth_resendCode.html
---
# Method: auth.resendCode
[Back to methods index](index.html)



Resend the login code via another medium, the phone code type is determined by the return value of the previous auth.sendCode/auth.resendCode: see [login](https://core.telegram.org/api/auth) for more info.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|phone\_number|[string](/API_docs/types/string.html) | The phone number | Optional|
|phone\_code\_hash|[string](/API_docs/types/string.html) | The phone code hash obtained from [auth.sendCode](../methods/auth.sendCode.html) | Optional|
|reason|[string](/API_docs/types/string.html) | Official clients only, used if the device integrity verification failed, and no secret could be obtained to invoke [auth.requestFirebaseSms](../methods/auth.requestFirebaseSms.html): in this case, the device integrity verification failure reason must be passed here. | Optional|


### Return type: [auth.SentCode](/API_docs/types/auth.SentCode.html)

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

$auth_SentCode = $MadelineProto->auth->resendCode(phone_number: 'string', phone_code_hash: 'string', reason: 'string', );
```

