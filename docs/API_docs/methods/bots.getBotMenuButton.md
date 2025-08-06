---
title: "bots.getBotMenuButton"
description: "Gets the menu button action for a given user or for all users, previously set using [bots.setBotMenuButton](../methods/bots.setBotMenuButton.html); users can see this information in the [botInfo](../constructors/botInfo.html) constructor."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/bots_getBotMenuButton.html
---
# Method: bots.getBotMenuButton
[Back to methods index](index.html)



Gets the menu button action for a given user or for all users, previously set using [bots.setBotMenuButton](../methods/bots.setBotMenuButton.html); users can see this information in the [botInfo](../constructors/botInfo.html) constructor.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|user\_id|[Username, chat ID, Update, Message or InputUser](/API_docs/types/InputUser.html) | User ID or empty for the default menu button. | Optional|


### Return type: [BotMenuButton](/API_docs/types/BotMenuButton.html)

### Can users use this method: **NO**


### Can bots use this method: **YES**


### Can bots use this method over a business connection with the `businessConnectionId` flag: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$BotMenuButton = $MadelineProto->bots->getBotMenuButton(user_id: $InputUser, );
```

