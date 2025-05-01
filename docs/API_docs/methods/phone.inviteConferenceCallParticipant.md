---
title: "phone.inviteConferenceCallParticipant"
description: "phone.inviteConferenceCallParticipant parameters, return type and example"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/phone_inviteConferenceCallParticipant.html
---
# Method: phone.inviteConferenceCallParticipant
[Back to methods index](index.html)



### Parameters:

| Name     |    Type       | Required |
|----------|---------------|----------|
|video|[Bool](/API_docs/types/Bool.html) | Optional|
|call|[InputGroupCall](/API_docs/types/InputGroupCall.html) | Yes|
|user\_id|[Username, chat ID, Update, Message or InputUser](/API_docs/types/InputUser.html) | Optional|


### Return type: [Updates](/API_docs/types/Updates.html)

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

$Updates = $MadelineProto->phone->inviteConferenceCallParticipant(video: $Bool, call: $InputGroupCall, user_id: $InputUser, );
```

