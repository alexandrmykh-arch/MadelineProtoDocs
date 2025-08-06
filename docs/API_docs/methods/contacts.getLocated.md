---
title: "contacts.getLocated"
description: "Get users and geochats near you, see [here »](https://core.telegram.org/api/nearby) for more info."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/contacts_getLocated.html
---
# Method: contacts.getLocated
[Back to methods index](index.html)



Get users and geochats near you, see [here »](https://core.telegram.org/api/nearby) for more info.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|background|[Bool](/API_docs/types/Bool.html) | While the geolocation of the current user is public, clients should update it in the background every half-an-hour or so, while setting this flag. <br>Do this only if the new location is more than 1 KM away from the previous one, or if the previous location is unknown. | Optional|
|geo\_point|[InputGeoPoint](/API_docs/types/InputGeoPoint.html) | Geolocation | Optional|
|self\_expires|[int](/API_docs/types/int.html) | If set, the geolocation of the current user will be public for the specified number of seconds; pass 0x7fffffff to disable expiry, 0 to make the current geolocation private; if the flag isn't set, no changes will be applied. | Optional|


### Return type: [Updates](/API_docs/types/Updates.html)

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

$Updates = $MadelineProto->contacts->getLocated(background: $Bool, geo_point: $InputGeoPoint, self_expires: $int, );
```

