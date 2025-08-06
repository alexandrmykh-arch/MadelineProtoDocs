---
title: "photos.updateProfilePhoto"
description: "Installs a previously uploaded photo as a profile photo."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/photos_updateProfilePhoto.html
---
# Method: photos.updateProfilePhoto
[Back to methods index](index.html)



Installs a previously uploaded photo as a profile photo.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|fallback|[Bool](/API_docs/types/Bool.html) | If set, the chosen profile photo will be shown to users that can't display your main profile photo due to your privacy settings. | Optional|
|bot|[Username, chat ID, Update, Message or InputUser](/API_docs/types/InputUser.html) | Can contain info of a bot we own, to change the profile photo of that bot, instead of the current user. | Optional|
|id|[MessageMedia, Update, Message or InputPhoto](/API_docs/types/InputPhoto.html) | Input photo | Optional|


### Return type: [photos.Photo](/API_docs/types/photos.Photo.html)

### Can users use this method: **YES**


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

$photos_Photo = $MadelineProto->photos->updateProfilePhoto(fallback: $Bool, bot: $InputUser, id: $InputPhoto, );
```

