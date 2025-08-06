---
title: "account.getGlobalPrivacySettings"
description: "Get global privacy settings"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/account_getGlobalPrivacySettings.html
---
# Method: account.getGlobalPrivacySettings
[Back to methods index](index.html)



Get global privacy settings



### Return type: [GlobalPrivacySettings](/API_docs/types/GlobalPrivacySettings.html)

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

$GlobalPrivacySettings = $MadelineProto->account->getGlobalPrivacySettings();
```

