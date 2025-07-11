---
title: "messages.sponsoredMessages"
description: "A set of sponsored messages associated to a channel"
nav_exclude: true
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/constructors/messages_sponsoredMessages.html
---
# Constructor: messages.sponsoredMessages  
[Back to constructors index](/API_docs/constructors/index.html)



A set of sponsored messages associated to a channel

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|posts\_between|[int](/API_docs/types/int.html) | Optional|If set, specifies the minimum number of messages between shown sponsored messages; otherwise, only one sponsored message must be shown after all ordinary messages.|
|start\_delay|[int](/API_docs/types/int.html) | Optional|
|between\_delay|[int](/API_docs/types/int.html) | Optional|
|messages|Array of [SponsoredMessage](/API_docs/types/SponsoredMessage.html) | Yes|Sponsored messages|
|chats|Array of [Chat](/API_docs/types/Chat.html) | Yes|Chats mentioned in the sponsored messages|
|users|Array of [User](/API_docs/types/User.html) | Yes|Users mentioned in the sponsored messages|



### Type: [messages.SponsoredMessages](/API_docs/types/messages.SponsoredMessages.html)


### Example:

```
$messages_sponsoredMessages = ['_' => 'messages.sponsoredMessages', 'posts_between' => int, 'start_delay' => int, 'between_delay' => int, 'messages' => [SponsoredMessage, SponsoredMessage], 'chats' => [Chat, Chat], 'users' => [User, User]];
```  
