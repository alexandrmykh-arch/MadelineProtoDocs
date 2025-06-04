---
title: "updateDraftMessage"
description: "Notifies a change of a message draft."
nav_exclude: true
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: updateDraftMessage  
[Back to constructors index](/API_docs/constructors/index.html)



Notifies a change of a message [draft](https://core.telegram.org/api/drafts).

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|peer|[long](/API_docs/types/long.html) | Yes|The peer to which the draft is associated|
|top\_msg\_id|[int](/API_docs/types/int.html) | Optional|ID of the [forum topic](https://core.telegram.org/api/forum#forum-topics) to which the draft is associated|
|saved\_peer\_id|[Peer](/API_docs/types/Peer.html) | Optional|
|draft|[DraftMessage](/API_docs/types/DraftMessage.html) | Optional|The draft|



### Type: [Update](/API_docs/types/Update.html)


### Example:

```
$updateDraftMessage = ['_' => 'updateDraftMessage', 'peer' => long, 'top_msg_id' => int, 'saved_peer_id' => Peer, 'draft' => DraftMessage];
```  
