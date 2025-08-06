---
title: "messages.getSearchResultsCalendar"
description: "Returns information about the next messages of the specified type in the chat split by days."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_getSearchResultsCalendar.html
---
# Method: messages.getSearchResultsCalendar
[Back to methods index](index.html)



Returns information about the next messages of the specified type in the chat split by days.

Returns the results in reverse chronological order.  
Can return partial results for the last returned day.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|peer|[Username, chat ID, Update, Message or InputPeer](/API_docs/types/InputPeer.html) | Peer where to search | Optional|
|saved\_peer\_id|[Username, chat ID, Update, Message or InputPeer](/API_docs/types/InputPeer.html) | Search within the [saved message dialog »](https://core.telegram.org/api/saved-messages) with this ID. | Optional|
|filter|[MessagesFilter](/API_docs/types/MessagesFilter.html) | Message filter, [inputMessagesFilterEmpty](../constructors/inputMessagesFilterEmpty.html), [inputMessagesFilterMyMentions](../constructors/inputMessagesFilterMyMentions.html) filters are not supported by this method. | Optional|
|offset\_id|[int](/API_docs/types/int.html) | [Offsets for pagination, for more info click here](https://core.telegram.org/api/offsets) | Optional|
|offset\_date|[int](/API_docs/types/int.html) | [Offsets for pagination, for more info click here](https://core.telegram.org/api/offsets) | Optional|


### Return type: [messages.SearchResultsCalendar](/API_docs/types/messages.SearchResultsCalendar.html)

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

$messages_SearchResultsCalendar = $MadelineProto->messages->getSearchResultsCalendar(peer: $InputPeer, saved_peer_id: $InputPeer, filter: $MessagesFilter, offset_id: $int, offset_date: $int, );
```

