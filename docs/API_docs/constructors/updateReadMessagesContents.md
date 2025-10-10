---
title: "updateReadMessagesContents"
description: "Contents of messages in the common message box were read (emitted specifically for messages like voice messages or video, only once the media is watched and marked as read using messages.readMessageContents)."
nav_exclude: true
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: updateReadMessagesContents  
[Back to constructors index](/API_docs/constructors/index.html)



Contents of messages in the common [message box](https://core.telegram.org/api/updates) were read (emitted specifically for messages like voice messages or video, only once the media is watched and marked as read using [messages.readMessageContents](../methods/messages.readMessageContents.html)).

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|messages|Array of [int](/API_docs/types/int.html) | Yes|IDs of read messages|
|pts|[int](/API_docs/types/int.html) | Yes|[Event count after generation](https://core.telegram.org/api/updates)|
|pts\_count|[int](/API_docs/types/int.html) | Yes|[Number of events that were generated](https://core.telegram.org/api/updates)|
|date|[int](/API_docs/types/int.html) | Optional|When was the last message in `messages` marked as read.|



### Type: [Update](/API_docs/types/Update.html)


### Example:

```
$updateReadMessagesContents = ['_' => 'updateReadMessagesContents', 'messages' => [int, int], 'pts' => int, 'pts_count' => int, 'date' => int];
```  
