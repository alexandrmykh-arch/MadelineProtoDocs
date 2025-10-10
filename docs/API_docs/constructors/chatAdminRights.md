---
title: "chatAdminRights"
description: "Represents the rights of an admin in a channel/supergroup."
nav_exclude: true
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: chatAdminRights  
[Back to constructors index](/API_docs/constructors/index.html)



Represents the rights of an admin in a [channel/supergroup](https://core.telegram.org/api/channel).

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|change\_info|[Bool](/API_docs/types/Bool.html) | Optional|If set, allows the admin to modify the description of the [channel/supergroup](https://core.telegram.org/api/channel)|
|post\_messages|[Bool](/API_docs/types/Bool.html) | Optional|If set, allows the admin to post messages in the [channel](https://core.telegram.org/api/channel)|
|edit\_messages|[Bool](/API_docs/types/Bool.html) | Optional|If set, allows the admin to also edit messages from other admins in the [channel](https://core.telegram.org/api/channel)|
|delete\_messages|[Bool](/API_docs/types/Bool.html) | Optional|If set, allows the admin to also delete messages from other admins in the [channel](https://core.telegram.org/api/channel)|
|ban\_users|[Bool](/API_docs/types/Bool.html) | Optional|If set, allows the admin to ban users from the [channel/supergroup](https://core.telegram.org/api/channel)|
|invite\_users|[Bool](/API_docs/types/Bool.html) | Optional|If set, allows the admin to invite users in the [channel/supergroup](https://core.telegram.org/api/channel)|
|pin\_messages|[Bool](/API_docs/types/Bool.html) | Optional|If set, allows the admin to pin messages in the [channel/supergroup](https://core.telegram.org/api/channel)|
|add\_admins|[Bool](/API_docs/types/Bool.html) | Optional|If set, allows the admin to add other admins with the same (or more limited) permissions in the [channel/supergroup](https://core.telegram.org/api/channel)|
|anonymous|[Bool](/API_docs/types/Bool.html) | Optional|Whether this admin is anonymous|
|manage\_call|[Bool](/API_docs/types/Bool.html) | Optional|If set, allows the admin to change group call/livestream settings|
|other|[Bool](/API_docs/types/Bool.html) | Optional|Set this flag if none of the other flags are set, but you still want the user to be an admin: if this or any of the other flags are set, the admin can get the chat [admin log](https://core.telegram.org/api/recent-actions), get [chat statistics](https://core.telegram.org/api/stats), get [message statistics in channels](https://core.telegram.org/api/stats), get channel members, see anonymous administrators in supergroups and ignore slow mode.|
|manage\_topics|[Bool](/API_docs/types/Bool.html) | Optional|If set, allows the admin to create, delete or modify [forum topics »](https://core.telegram.org/api/forum#forum-topics).|
|post\_stories|[Bool](/API_docs/types/Bool.html) | Optional|If set, allows the admin to post [stories](https://core.telegram.org/api/stories) as the [channel](https://core.telegram.org/api/channel).|
|edit\_stories|[Bool](/API_docs/types/Bool.html) | Optional|If set, allows the admin to edit [stories](https://core.telegram.org/api/stories) posted by the other admins of the [channel](https://core.telegram.org/api/channel).|
|delete\_stories|[Bool](/API_docs/types/Bool.html) | Optional|If set, allows the admin to delete [stories](https://core.telegram.org/api/stories) posted by the other admins of the [channel](https://core.telegram.org/api/channel).|
|manage\_direct\_messages|[Bool](/API_docs/types/Bool.html) | Optional|If set, allows the admin to manage the [direct messages monoforum »](https://core.telegram.org/api/monoforum) and [decline suggested posts »](https://core.telegram.org/api/suggested-posts).|



### Type: [ChatAdminRights](/API_docs/types/ChatAdminRights.html)


### Example:

```
$chatAdminRights = ['_' => 'chatAdminRights', 'change_info' => Bool, 'post_messages' => Bool, 'edit_messages' => Bool, 'delete_messages' => Bool, 'ban_users' => Bool, 'invite_users' => Bool, 'pin_messages' => Bool, 'add_admins' => Bool, 'anonymous' => Bool, 'manage_call' => Bool, 'other' => Bool, 'manage_topics' => Bool, 'post_stories' => Bool, 'edit_stories' => Bool, 'delete_stories' => Bool, 'manage_direct_messages' => Bool];
```  
