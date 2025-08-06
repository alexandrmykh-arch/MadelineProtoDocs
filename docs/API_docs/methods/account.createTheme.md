---
title: "account.createTheme"
description: "Create a theme"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/account_createTheme.html
---
# Method: account.createTheme
[Back to methods index](index.html)



Create a theme

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|slug|[string](/API_docs/types/string.html) | Unique theme ID used to generate [theme deep links](https://core.telegram.org/api/links#theme-links), can be empty to autogenerate a random ID. | Optional|
|title|[string](/API_docs/types/string.html) | Theme name | Optional|
|document|[MessageMedia, Update, Message or InputDocument](/API_docs/types/InputDocument.html) | Theme file | Optional|
|settings|Array of [InputThemeSettings](/API_docs/types/InputThemeSettings.html) | Theme settings, multiple values can be provided for the different base themes (day/night mode, etc). | Optional|


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

$Theme = $MadelineProto->account->createTheme(slug: 'string', title: 'string', document: $InputDocument, settings: [$InputThemeSettings, $InputThemeSettings], );
```

