---
title: "messages.updateDialogFilter"
description: "Update [folder](https://core.telegram.org/api/folders)"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_updateDialogFilter.html
---
# Method: messages.updateDialogFilter
[Back to methods index](index.html)



Update [folder](https://core.telegram.org/api/folders)

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|id|[int](/API_docs/types/int.html) | [Folder](https://core.telegram.org/api/folders) ID | Optional|
|filter|[DialogFilter](/API_docs/types/DialogFilter.html) | [Folder](https://core.telegram.org/api/folders) info | Optional|


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

$Bool = $MadelineProto->messages->updateDialogFilter(id: $int, filter: $DialogFilter, );
```

