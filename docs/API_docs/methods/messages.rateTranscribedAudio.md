---
title: "messages.rateTranscribedAudio"
description: "Rate [transcribed voice message](https://core.telegram.org/api/transcribe)"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_rateTranscribedAudio.html
---
# Method: messages.rateTranscribedAudio
[Back to methods index](index.html)



Rate [transcribed voice message](https://core.telegram.org/api/transcribe)

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|peer|[Username, chat ID, Update, Message or InputPeer](/API_docs/types/InputPeer.html) | Peer where the voice message was sent | Optional|
|msg\_id|[int](/API_docs/types/int.html) | Message ID | Optional|
|transcription\_id|[long](/API_docs/types/long.html) | Transcription ID | Yes|
|good|[Bool](/API_docs/types/Bool.html) | Whether the transcription was correct | Yes|


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

$Bool = $MadelineProto->messages->rateTranscribedAudio(peer: $InputPeer, msg_id: $int, transcription_id: $long, good: $Bool, );
```

