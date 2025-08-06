---
title: "account.saveAutoDownloadSettings"
description: "Change media autodownload settings"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/account_saveAutoDownloadSettings.html
---
# Method: account.saveAutoDownloadSettings
[Back to methods index](index.html)



Change media autodownload settings

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|low|[Bool](/API_docs/types/Bool.html) | Whether to save media in the low data usage preset | Optional|
|high|[Bool](/API_docs/types/Bool.html) | Whether to save media in the high data usage preset | Optional|
|settings|[AutoDownloadSettings](/API_docs/types/AutoDownloadSettings.html) | Media autodownload settings | Yes|


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

$Bool = $MadelineProto->account->saveAutoDownloadSettings(low: $Bool, high: $Bool, settings: $AutoDownloadSettings, );
```

