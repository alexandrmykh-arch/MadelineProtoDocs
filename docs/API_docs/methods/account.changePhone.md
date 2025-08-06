---
title: "account.changePhone"
description: "Change the phone number of the current account"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/account_changePhone.html
---
# Method: account.changePhone
[Back to methods index](index.html)



Change the phone number of the current account

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|phone\_number|[string](/API_docs/types/string.html) | New phone number | Optional|
|phone\_code\_hash|[string](/API_docs/types/string.html) | Phone code hash received when calling [account.sendChangePhoneCode](../methods/account.sendChangePhoneCode.html) | Optional|
|phone\_code|[string](/API_docs/types/string.html) | Phone code received when calling [account.sendChangePhoneCode](../methods/account.sendChangePhoneCode.html) | Optional|


### Return type: [User](/API_docs/types/User.html)

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

$User = $MadelineProto->account->changePhone(phone_number: 'string', phone_code_hash: 'string', phone_code: 'string', );
```

