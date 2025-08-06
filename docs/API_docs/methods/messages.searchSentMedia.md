---
title: "messages.searchSentMedia"
description: "View and search recently sent media.  "
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_searchSentMedia.html
---
# Method: messages.searchSentMedia
[Back to methods index](index.html)



View and search recently sent media.  
This method does not support pagination.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|q|[string](/API_docs/types/string.html) | Optional search query | Optional|
|filter|[MessagesFilter](/API_docs/types/MessagesFilter.html) | Message filter | Optional|
|limit|[int](/API_docs/types/int.html) | Maximum number of results to return (max 100). | Optional|


### Return type: [messages.Messages](/API_docs/types/messages.Messages.html)

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

$messages_Messages = $MadelineProto->messages->searchSentMedia(q: 'string', filter: $MessagesFilter, limit: $int, );
```

