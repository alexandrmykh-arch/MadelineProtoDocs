---
title: "account.saveWallPaper"
description: "Install/uninstall [wallpaper](https://core.telegram.org/api/wallpapers)"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/account_saveWallPaper.html
---
# Method: account.saveWallPaper
[Back to methods index](index.html)



Install/uninstall [wallpaper](https://core.telegram.org/api/wallpapers)

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|wallpaper|[InputWallPaper](/API_docs/types/InputWallPaper.html) | [Wallpaper](https://core.telegram.org/api/wallpapers) to install or uninstall | Yes|
|unsave|[Bool](/API_docs/types/Bool.html) | Uninstall wallpaper? | Yes|
|settings|[WallPaperSettings](/API_docs/types/WallPaperSettings.html) | Wallpaper settings | Yes|


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

$Bool = $MadelineProto->account->saveWallPaper(wallpaper: $InputWallPaper, unsave: $Bool, settings: $WallPaperSettings, );
```

