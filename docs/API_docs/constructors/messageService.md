---
title: "messageService"
description: "Indicates a service message"
nav_exclude: true
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: messageService  
[Back to constructors index](/API_docs/constructors/index.html)



Indicates a service message

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|out|[Bool](/API_docs/types/Bool.html) | Optional|Whether the message is outgoing|
|mentioned|[Bool](/API_docs/types/Bool.html) | Optional|Whether we were mentioned in the message|
|media\_unread|[Bool](/API_docs/types/Bool.html) | Optional|Whether the message contains unread media|
|reactions\_are\_possible|[Bool](/API_docs/types/Bool.html) | Optional|Whether you can [react to this message »](https://core.telegram.org/api/reactions).|
|silent|[Bool](/API_docs/types/Bool.html) | Optional|Whether the message is silent|
|post|[Bool](/API_docs/types/Bool.html) | Optional|Whether it's a channel post|
|legacy|[Bool](/API_docs/types/Bool.html) | Optional|This is a legacy message: it has to be refetched with the new layer|
|id|[int](/API_docs/types/int.html) | Yes|Message ID|
|from\_id|[Peer](/API_docs/types/Peer.html) | Optional|ID of the sender of this message|
|peer\_id|[Peer](/API_docs/types/Peer.html) | Yes|Sender of service message|
|saved\_peer\_id|[Peer](/API_docs/types/Peer.html) | Optional|Will only be set for service messages within a [monoforum topic »](https://core.telegram.org/api/monoforum): `peer` will be equal to the ID of the monoforum and the `saved_peer_id` flag will be set to the ID of a topic.|
|reply\_to|[MessageReplyHeader](/API_docs/types/MessageReplyHeader.html) | Optional|Reply (thread) information|
|date|[int](/API_docs/types/int.html) | Yes|Message date|
|action|[MessageAction](/API_docs/types/MessageAction.html) | Optional|Event connected with the service message|
|reactions|[MessageReactions](/API_docs/types/MessageReactions.html) | Optional|[Reactions »](https://core.telegram.org/api/reactions).|
|ttl\_period|[int](/API_docs/types/int.html) | Optional|Time To Live of the message, once message.date+message.ttl\_period === time(), the message will be deleted on the server, and must be deleted locally as well.|



### Type: [Message](/API_docs/types/Message.html)


### Example:

```
$messageService = ['_' => 'messageService', 'out' => Bool, 'mentioned' => Bool, 'media_unread' => Bool, 'reactions_are_possible' => Bool, 'silent' => Bool, 'post' => Bool, 'legacy' => Bool, 'id' => int, 'from_id' => Peer, 'peer_id' => Peer, 'saved_peer_id' => Peer, 'reply_to' => MessageReplyHeader, 'date' => int, 'action' => MessageAction, 'reactions' => MessageReactions, 'ttl_period' => int];
```  
