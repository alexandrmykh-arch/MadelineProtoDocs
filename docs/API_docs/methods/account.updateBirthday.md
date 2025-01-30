---
title: "account.updateBirthday"
description: "Update our [birthday, see here »](https://core.telegram.org/api/profile#birthday) for more info."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/account_updateBirthday.html
---
# Method: account.updateBirthday
[Back to methods index](index.html)



Update our [birthday, see here »](https://core.telegram.org/api/profile#birthday) for more info.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|birthday|[Birthday](/API_docs/types/Birthday.html) | Birthday. | Optional|


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

$Bool = $MadelineProto->account->updateBirthday(birthday: $Birthday, );
```

