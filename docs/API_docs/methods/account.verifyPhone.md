---
title: "account.verifyPhone"
description: "Verify a phone number for telegram [passport](https://core.telegram.org/passport)."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/account_verifyPhone.html
---
# Method: account.verifyPhone
[Back to methods index](index.html)



Verify a phone number for telegram [passport](https://core.telegram.org/passport).

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|phone\_number|[string](/API_docs/types/string.html) | Phone number | Optional|
|phone\_code\_hash|[string](/API_docs/types/string.html) | Phone code hash received from the call to [account.sendVerifyPhoneCode](../methods/account.sendVerifyPhoneCode.html) | Optional|
|phone\_code|[string](/API_docs/types/string.html) | Code received after the call to [account.sendVerifyPhoneCode](../methods/account.sendVerifyPhoneCode.html) | Optional|


### Return type: [Bool](/API_docs/types/Bool.html)

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

$Bool = $MadelineProto->account->verifyPhone(phone_number: 'string', phone_code_hash: 'string', phone_code: 'string', );
```

