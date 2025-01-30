---
title: "messages.uploadMedia"
description: "Upload a file and associate it to a chat (without actually sending it to the chat)"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_uploadMedia.html
---
# Method: messages.uploadMedia
[Back to methods index](index.html)



Upload a file and associate it to a chat (without actually sending it to the chat)

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|business\_connection\_id|[string](/API_docs/types/string.html) | Whether the media will be used only in the specified [business connection »](https://core.telegram.org/api/business#connected-bots), and not directly by the bot. | Optional|
|peer|[Username, chat ID, Update, Message or InputPeer](/API_docs/types/InputPeer.html) | The chat, can be [inputPeerEmpty](../constructors/inputPeerEmpty.html) for bots and [inputPeerSelf](../constructors/inputPeerSelf.html) for users. | Optional|
|media|[MessageMedia, Update, Message or InputMedia](/API_docs/types/InputMedia.html) | File uploaded in chunks as described in [files »](https://core.telegram.org/api/files) | Optional|


### Return type: [MessageMedia](/API_docs/types/MessageMedia.html)

### Can userbots use this method: **YES**

### Can bots use this method: **YES**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$MessageMedia = $MadelineProto->messages->uploadMedia(business_connection_id: 'string', peer: $InputPeer, media: $InputMedia, );
```

