---
title: "users.getIsPremiumRequiredToContact"
description: "Check whether we can write to the specified user (this method can only be called by non-[Premium](https://core.telegram.org/api/premium) users), see [here »](https://core.telegram.org/api/privacy#require-premium-for-new-non-contact-users) for more info on the full flow."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/users_getIsPremiumRequiredToContact.html
---
# Method: users.getIsPremiumRequiredToContact
[Back to methods index](index.html)



Check whether we can write to the specified user (this method can only be called by non-[Premium](https://core.telegram.org/api/premium) users), see [here »](https://core.telegram.org/api/privacy#require-premium-for-new-non-contact-users) for more info on the full flow.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|id|Array of [Username, chat ID, Update, Message or InputUser](/API_docs/types/InputUser.html) | Users to fetch info about. | Yes|


### Return type: [Vector\_of\_Bool](/API_docs/types/Bool.html)

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

$Vector_of_Bool = $MadelineProto->users->getIsPremiumRequiredToContact(id: [$InputUser, $InputUser], );
```

