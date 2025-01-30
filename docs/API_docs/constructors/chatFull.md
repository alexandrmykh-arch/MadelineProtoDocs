---
title: "chatFull"
description: "Full info about a basic group."
nav_exclude: true
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: chatFull  
[Back to constructors index](/API_docs/constructors/index.html)



Full info about a [basic group](https://core.telegram.org/api/channel#basic-groups).

When updating the [local peer database »](https://core.telegram.org/api/peers), all fields from the newly received constructor take priority over the old constructor cached locally (including by removing fields that aren't set in the new constructor).

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|can\_set\_username|[Bool](/API_docs/types/Bool.html) | Optional|Can we change the username of this chat|
|has\_scheduled|[Bool](/API_docs/types/Bool.html) | Optional|Whether [scheduled messages](https://core.telegram.org/api/scheduled-messages) are available|
|translations\_disabled|[Bool](/API_docs/types/Bool.html) | Optional|Whether the [real-time chat translation popup](https://core.telegram.org/api/translation) should be hidden.|
|id|[long](/API_docs/types/long.html) | Yes|ID of the chat|
|about|[string](/API_docs/types/string.html) | Yes|About string for this chat|
|participants|[ChatParticipants](/API_docs/types/ChatParticipants.html) | Yes|Participant list|
|chat\_photo|[Photo](/API_docs/types/Photo.html) | Optional|Chat photo|
|notify\_settings|[PeerNotifySettings](/API_docs/types/PeerNotifySettings.html) | Yes|Notification settings|
|exported\_invite|[ExportedChatInvite](/API_docs/types/ExportedChatInvite.html) | Optional|Chat invite|
|bot\_info|Array of [BotInfo](/API_docs/types/BotInfo.html) | Optional|Info about bots that are in this chat|
|pinned\_msg\_id|[int](/API_docs/types/int.html) | Optional|Message ID of the last [pinned message](https://core.telegram.org/api/pin)|
|folder\_id|[int](/API_docs/types/int.html) | Optional|[Peer folder ID, for more info click here](https://core.telegram.org/api/folders#peer-folders)|
|call|[InputGroupCall](/API_docs/types/InputGroupCall.html) | Optional|Group call information|
|ttl\_period|[int](/API_docs/types/int.html) | Optional|Time-To-Live of messages sent by the current user to this chat|
|groupcall\_default\_join\_as|[Peer](/API_docs/types/Peer.html) | Optional|When using [phone.getGroupCallJoinAs](../methods/phone.getGroupCallJoinAs.html) to get a list of peers that can be used to join a group call, this field indicates the peer that should be selected by default.|
|theme\_emoticon|[string](/API_docs/types/string.html) | Optional|Emoji representing a specific chat theme|
|requests\_pending|[int](/API_docs/types/int.html) | Optional|Pending [join requests »](https://core.telegram.org/api/invites#join-requests)|
|recent\_requesters|Array of [long](/API_docs/types/long.html) | Optional|IDs of users who requested to join recently|
|available\_reactions|[ChatReactions](/API_docs/types/ChatReactions.html) | Optional|Allowed [message reactions »](https://core.telegram.org/api/reactions)|
|reactions\_limit|[int](/API_docs/types/int.html) | Optional|This flag may be used to impose a custom limit of unique reactions (i.e. a customizable version of [appConfig.reactions\_uniq\_max](https://core.telegram.org/api/config#reactions-uniq-max)).|



### Type: [ChatFull](/API_docs/types/ChatFull.html)


### Example:

```
$chatFull = ['_' => 'chatFull', 'can_set_username' => Bool, 'has_scheduled' => Bool, 'translations_disabled' => Bool, 'id' => long, 'about' => 'string', 'participants' => ChatParticipants, 'chat_photo' => Photo, 'notify_settings' => PeerNotifySettings, 'exported_invite' => ExportedChatInvite, 'bot_info' => [BotInfo, BotInfo], 'pinned_msg_id' => int, 'folder_id' => int, 'call' => InputGroupCall, 'ttl_period' => int, 'groupcall_default_join_as' => Peer, 'theme_emoticon' => 'string', 'requests_pending' => int, 'recent_requesters' => [long, long], 'available_reactions' => ChatReactions, 'reactions_limit' => int];
```  
