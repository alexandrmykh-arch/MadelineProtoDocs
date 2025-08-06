---
title: "bots.setBotCommands"
description: "Set bot command list"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/bots_setBotCommands.html
---
# Method: bots.setBotCommands
[Back to methods index](index.html)



Set bot command list

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|scope|[BotCommandScope](/API_docs/types/BotCommandScope.html) | Command scope | Yes|
|lang\_code|[string](/API_docs/types/string.html) | Language code | Optional|
|commands|Array of [BotCommand](/API_docs/types/BotCommand.html) | Bot commands | Yes|


### Return type: [Bool](/API_docs/types/Bool.html)

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

$Bool = $MadelineProto->bots->setBotCommands(scope: $BotCommandScope, lang_code: 'string', commands: [$BotCommand, $BotCommand], );
```

