---
title: "help.dismissSuggestion"
description: "Dismiss a [suggestion, see here for more info »](https://core.telegram.org/api/config#suggestions)."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/help_dismissSuggestion.html
---
# Method: help.dismissSuggestion
[Back to methods index](index.html)



Dismiss a [suggestion, see here for more info »](https://core.telegram.org/api/config#suggestions).

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|peer|[Username, chat ID, Update, Message or InputPeer](/API_docs/types/InputPeer.html) | In the case of pending suggestions in [channels](../constructors/channelFull.html), the channel ID. | Optional|
|suggestion|[string](/API_docs/types/string.html) | [Suggestion, see here for more info »](https://core.telegram.org/api/config#suggestions). | Optional|


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

$Bool = $MadelineProto->help->dismissSuggestion(peer: $InputPeer, suggestion: 'string', );
```

