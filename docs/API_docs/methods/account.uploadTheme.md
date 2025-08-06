---
title: "account.uploadTheme"
description: "Upload theme"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/account_uploadTheme.html
---
# Method: account.uploadTheme
[Back to methods index](index.html)



Upload theme

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|file|[File path or InputFile](/API_docs/types/InputFile.html) | [Previously uploaded](https://core.telegram.org/api/themes#uploading-theme-files) theme file with platform-specific colors for UI components, can be left unset when creating themes that only modify the wallpaper or accent colors. | Yes|
|thumb|[File path or InputFile](/API_docs/types/InputFile.html) | Thumbnail | Optional|
|file\_name|[string](/API_docs/types/string.html) | File name | Optional|
|mime\_type|[string](/API_docs/types/string.html) | MIME type, must be `application/x-tgtheme-{format}`, where `format` depends on the client | Optional|


### Return type: [Document](/API_docs/types/Document.html)

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

$Document = $MadelineProto->account->uploadTheme(file: $InputFile, thumb: $InputFile, file_name: 'string', mime_type: 'string', );
```

