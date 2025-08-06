---
title: "auth.signIn"
description: "You cannot use this method directly, use the completePhoneLogin method instead (see https://docs.madelineproto.xyz for more info)"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/auth_signIn.html
---
# Method: auth.signIn
[Back to methods index](index.html)



You cannot use this method directly, use the completePhoneLogin method instead (see https://docs.madelineproto.xyz for more info)

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|phone\_number|[string](/API_docs/types/string.html) | Phone number in the international format | Optional|
|phone\_code\_hash|[string](/API_docs/types/string.html) | SMS-message ID, obtained from [auth.sendCode](../methods/auth.sendCode.html) | Optional|
|phone\_code|[string](/API_docs/types/string.html) | Valid numerical code from the SMS-message | Optional|
|email\_verification|[EmailVerification](/API_docs/types/EmailVerification.html) | Email verification code or token | Optional|


### Return type: [auth.Authorization](/API_docs/types/auth.Authorization.html)

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

$auth_Authorization = $MadelineProto->auth->signIn(phone_number: 'string', phone_code_hash: 'string', phone_code: 'string', email_verification: $EmailVerification, );
```

