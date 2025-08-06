---
title: "account.getTheme"
description: "Get theme information"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/account_getTheme.html
---
# Method: account.getTheme
[Back to methods index](index.html)



Get theme information

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|format|[string](/API_docs/types/string.html) | Theme format, a string that identifies the theming engines supported by the client | Optional|
|theme|[InputTheme](/API_docs/types/InputTheme.html) | Theme | Yes|


### Return type: [Theme](/API_docs/types/Theme.html)

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

$Theme = $MadelineProto->account->getTheme(format: 'string', theme: $InputTheme, );
```

