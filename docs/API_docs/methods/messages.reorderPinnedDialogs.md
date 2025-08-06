---
title: "messages.reorderPinnedDialogs"
description: "Reorder pinned dialogs"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_reorderPinnedDialogs.html
---
# Method: messages.reorderPinnedDialogs
[Back to methods index](index.html)



Reorder pinned dialogs

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|force|[Bool](/API_docs/types/Bool.html) | If set, dialogs pinned server-side but not present in the `order` field will be unpinned. | Optional|
|folder\_id|[int](/API_docs/types/int.html) | [Peer folder ID, for more info click here](https://core.telegram.org/api/folders#peer-folders) | Optional|
|order|Array of [InputDialogPeer](/API_docs/types/InputDialogPeer.html) | New dialog order | Yes|


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

$Bool = $MadelineProto->messages->reorderPinnedDialogs(force: $Bool, folder_id: $int, order: [$InputDialogPeer, $InputDialogPeer], );
```

