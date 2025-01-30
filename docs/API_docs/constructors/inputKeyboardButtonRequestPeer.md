---
title: "inputKeyboardButtonRequestPeer"
description: "Prompts the user to select and share one or more peers with the bot using messages.sendBotRequestedPeer."
nav_exclude: true
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: inputKeyboardButtonRequestPeer  
[Back to constructors index](/API_docs/constructors/index.html)



Prompts the user to select and share one or more peers with the bot using [messages.sendBotRequestedPeer](../methods/messages.sendBotRequestedPeer.html).

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|name\_requested|[Bool](/API_docs/types/Bool.html) | Optional|Set this flag to request the peer's name.|
|username\_requested|[Bool](/API_docs/types/Bool.html) | Optional|Set this flag to request the peer's `@username` (if any).|
|photo\_requested|[Bool](/API_docs/types/Bool.html) | Optional|Set this flag to request the peer's photo (if any).|
|text|[string](/API_docs/types/string.html) | Yes|Button text|
|button\_id|[int](/API_docs/types/int.html) | Yes|Button ID, to be passed to [messages.sendBotRequestedPeer](../methods/messages.sendBotRequestedPeer.html).|
|peer\_type|[RequestPeerType](/API_docs/types/RequestPeerType.html) | Yes|Filtering criteria to use for the peer selection list shown to the user. <br>The list should display all existing peers of the specified type, and should also offer an option for the user to create and immediately use one or more (up to `max_quantity`) peers of the specified type, if needed.|
|max\_quantity|[int](/API_docs/types/int.html) | Yes|Maximum number of peers that can be chosen.|



### Type: [KeyboardButton](/API_docs/types/KeyboardButton.html)


### Example:

```
$inputKeyboardButtonRequestPeer = ['_' => 'inputKeyboardButtonRequestPeer', 'name_requested' => Bool, 'username_requested' => Bool, 'photo_requested' => Bool, 'text' => 'string', 'button_id' => int, 'peer_type' => RequestPeerType, 'max_quantity' => int];
```  
