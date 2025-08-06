---
title: "phone.checkGroupCall"
description: "Check whether the group call Server Forwarding Unit is currently receiving the streams with the specified WebRTC source IDs.  "
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/phone_checkGroupCall.html
---
# Method: phone.checkGroupCall
[Back to methods index](index.html)



Check whether the group call Server Forwarding Unit is currently receiving the streams with the specified WebRTC source IDs.  
Returns an intersection of the source IDs specified in `sources`, and the source IDs currently being forwarded by the SFU.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|call|[InputGroupCall](/API_docs/types/InputGroupCall.html) | Group call | Yes|
|sources|Array of [int](/API_docs/types/int.html) | Source IDs | Yes|


### Return type: [Vector\_of\_int](/API_docs/types/int.html)

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

$Vector_of_int = $MadelineProto->phone->checkGroupCall(call: $InputGroupCall, sources: [$int, $int], );
```

