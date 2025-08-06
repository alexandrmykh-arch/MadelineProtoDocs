---
title: "help.getDeepLinkInfo"
description: "Get info about an unsupported deep link, see [here for more info »](https://core.telegram.org/api/links#unsupported-links)."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/help_getDeepLinkInfo.html
---
# Method: help.getDeepLinkInfo
[Back to methods index](index.html)



Get info about an unsupported deep link, see [here for more info »](https://core.telegram.org/api/links#unsupported-links).

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|path|[string](/API_docs/types/string.html) | Path component of a `tg:` link | Optional|


### Return type: [help.DeepLinkInfo](/API_docs/types/help.DeepLinkInfo.html)

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

$help_DeepLinkInfo = $MadelineProto->help->getDeepLinkInfo(path: 'string', );
```

