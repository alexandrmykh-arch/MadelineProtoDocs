---
title: "account.setReactionsNotifySettings"
description: "Change the [reaction notification settings »](https://core.telegram.org/api/reactions#notifications-about-reactions)."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/account_setReactionsNotifySettings.html
---
# Method: account.setReactionsNotifySettings
[Back to methods index](index.html)



Change the [reaction notification settings »](https://core.telegram.org/api/reactions#notifications-about-reactions).

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|settings|[ReactionsNotifySettings](/API_docs/types/ReactionsNotifySettings.html) | New reaction notification settings. | Yes|


### Return type: [ReactionsNotifySettings](/API_docs/types/ReactionsNotifySettings.html)

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

$ReactionsNotifySettings = $MadelineProto->account->setReactionsNotifySettings(settings: $ReactionsNotifySettings, );
```

