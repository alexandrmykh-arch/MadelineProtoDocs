---
title: "contacts.getBlocked"
description: "Returns the list of blocked users."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/contacts_getBlocked.html
---
# Method: contacts.getBlocked
[Back to methods index](index.html)



Returns the list of blocked users.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|my\_stories\_from|[Bool](/API_docs/types/Bool.html) | Whether to fetch the story blocklist; if not set, will fetch the main blocklist. See [here »](https://core.telegram.org/api/block) for differences between the two. | Optional|
|offset|[int](/API_docs/types/int.html) | The number of list elements to be skipped | Optional|
|limit|[int](/API_docs/types/int.html) | The number of list elements to be returned | Optional|


### Return type: [contacts.Blocked](/API_docs/types/contacts.Blocked.html)

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

$contacts_Blocked = $MadelineProto->contacts->getBlocked(my_stories_from: $Bool, offset: $int, limit: $int, );
```

