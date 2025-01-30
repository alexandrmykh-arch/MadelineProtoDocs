---
title: "message"
description: "A message"
nav_exclude: true
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: message  
[Back to constructors index](/API_docs/constructors/index.html)



A message

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|out|[Bool](/API_docs/types/Bool.html) | Optional|Is this an outgoing message|
|mentioned|[Bool](/API_docs/types/Bool.html) | Optional|Whether we were [mentioned](https://core.telegram.org/api/mentions) in this message|
|media\_unread|[Bool](/API_docs/types/Bool.html) | Optional|Whether there are unread media attachments in this message|
|silent|[Bool](/API_docs/types/Bool.html) | Optional|Whether this is a silent message (no notification triggered)|
|post|[Bool](/API_docs/types/Bool.html) | Optional|Whether this is a channel post|
|from\_scheduled|[Bool](/API_docs/types/Bool.html) | Optional|Whether this is a [scheduled message](https://core.telegram.org/api/scheduled-messages)|
|legacy|[Bool](/API_docs/types/Bool.html) | Optional|This is a legacy message: it has to be refetched with the new layer|
|edit\_hide|[Bool](/API_docs/types/Bool.html) | Optional|Whether the message should be shown as not modified to the user, even if an edit date is present|
|pinned|[Bool](/API_docs/types/Bool.html) | Optional|Whether this message is [pinned](https://core.telegram.org/api/pin)|
|noforwards|[Bool](/API_docs/types/Bool.html) | Optional|Whether this message is [protected](https://telegram.org/blog/protected-content-delete-by-date-and-more) and thus cannot be forwarded; clients should also prevent users from saving attached media (i.e. videos should only be streamed, photos should be kept in RAM, et cetera).|
|invert\_media|[Bool](/API_docs/types/Bool.html) | Optional|If set, any eventual webpage preview will be shown on top of the message instead of at the bottom.|
|offline|[Bool](/API_docs/types/Bool.html) | Optional|
|video\_processing\_pending|[Bool](/API_docs/types/Bool.html) | Optional|
|id|[int](/API_docs/types/int.html) | Yes|ID of the message|
|from\_id|[Peer](/API_docs/types/Peer.html) | Optional|ID of the sender of the message|
|from\_boosts\_applied|[int](/API_docs/types/int.html) | Optional|Supergroups only, contains the number of [boosts](https://core.telegram.org/api/boost) this user has given the current supergroup, and should be shown in the UI in the header of the message. <br>Only present for incoming messages from non-anonymous supergroup members that have boosted the supergroup. <br>Note that this counter should be locally overridden for non-anonymous *outgoing* messages, according to the current value of [channelFull](../constructors/channelFull.html).`boosts_applied`, to ensure the value is correct even for messages sent by the current user before a supergroup was boosted (or after a boost has expired or the number of boosts has changed); do not update this value for incoming messages from other users, even if their boosts have changed.|
|peer\_id|[Peer](/API_docs/types/Peer.html) | Yes|Peer ID, the chat where this message was sent|
|saved\_peer\_id|[Peer](/API_docs/types/Peer.html) | Optional|Messages fetched from a [saved messages dialog »](https://core.telegram.org/api/saved-messages) will have `peer`=[inputPeerSelf](../constructors/inputPeerSelf.html) and the `saved_peer_id` flag set to the ID of the saved dialog.<br>|
|fwd\_from|[MessageFwdHeader](/API_docs/types/MessageFwdHeader.html) | Optional|Info about forwarded messages|
|via\_bot\_id|[long](/API_docs/types/long.html) | Optional|ID of the inline bot that generated the message|
|via\_business\_bot\_id|[long](/API_docs/types/long.html) | Optional|
|reply\_to|[MessageReplyHeader](/API_docs/types/MessageReplyHeader.html) | Optional|Reply information|
|date|[int](/API_docs/types/int.html) | Yes|Date of the message|
|message|[string](/API_docs/types/string.html) | Yes|The message|
|media|[MessageMedia](/API_docs/types/MessageMedia.html) | Optional|Media attachment|
|reply\_markup|[ReplyMarkup](/API_docs/types/ReplyMarkup.html) | Optional|Reply markup (bot/inline keyboards)|
|entities|Array of [MessageEntity](/API_docs/types/MessageEntity.html) | Optional|Message [entities](https://core.telegram.org/api/entities) for styled text|
|parse\_mode| [string](/API_docs/types/string.html) | Whether to parse HTML or Markdown markup in the message| Optional |
|views|[int](/API_docs/types/int.html) | Optional|View count for channel posts|
|forwards|[int](/API_docs/types/int.html) | Optional|Forward counter|
|replies|[MessageReplies](/API_docs/types/MessageReplies.html) | Optional|Info about [post comments (for channels) or message replies (for groups)](https://core.telegram.org/api/threads)|
|edit\_date|[int](/API_docs/types/int.html) | Optional|Last edit date of this message|
|post\_author|[string](/API_docs/types/string.html) | Optional|Name of the author of this message for channel posts (with signatures enabled)|
|grouped\_id|[long](/API_docs/types/long.html) | Optional|Multiple media messages sent using [messages.sendMultiMedia](../methods/messages.sendMultiMedia.html) with the same grouped ID indicate an [album or media group](https://core.telegram.org/api/files#albums-grouped-media)|
|reactions|[MessageReactions](/API_docs/types/MessageReactions.html) | Optional|Reactions to this message|
|restriction\_reason|Array of [RestrictionReason](/API_docs/types/RestrictionReason.html) | Optional|Contains the reason why access to this message must be restricted.|
|ttl\_period|[int](/API_docs/types/int.html) | Optional|Time To Live of the message, once message.date+message.ttl\_period === time(), the message will be deleted on the server, and must be deleted locally as well.|
|quick\_reply\_shortcut\_id|[int](/API_docs/types/int.html) | Optional|If set, this message is a [quick reply shortcut message »](https://core.telegram.org/api/business#quick-reply-shortcuts) (note that quick reply shortcut messages *sent* to a private chat will *not* have this field set).|
|effect|[long](/API_docs/types/long.html) | Optional|
|factcheck|[FactCheck](/API_docs/types/FactCheck.html) | Optional|
|report\_delivery\_until\_date|[int](/API_docs/types/int.html) | Optional|



### Type: [Message](/API_docs/types/Message.html)



## Usage of parse_mode:

Set parse_mode to html to enable HTML parsing of the message.  

Set parse_mode to Markdown to enable markdown parsing of the message.  

The following tags are currently supported:

```html
<br>a newline
<b><i>bold works ok, internal tags are stripped</i> </b>
<strong>bold</strong>
<em>italic</em>
<i>italic</i>
<u>underline</u>
<s>strikethrough</s>
<del>strikethrough</del>
<strike>strikethrough</strike>
<code>inline fixed-width code</code>
<pre>pre-formatted fixed-width code block</pre>
<blockquote>pre-formatted fixed-width code block</blockquote>
<a href="https://github.com">URL</a>
<a href="mention:@danogentili">Mention by username</a>
<a href="mention:186785362">Mention by user id</a>
<a href="tg://user?id=186785362">Mention by user id</a>
Custom emoji: <emoji id="5368324170671202286">👍</emoji>
Custom emoji: <tg-emoji emoji-id="5368324170671202286">👍</tg-emoji>
<pre language="json">Pre tags can have a language attribute</pre>
<spoiler>Spoiler</spoiler>
<tg-spoiler>Spoiler</tg-spoiler>
```

You can also use normal markdown ([bot API MarkdownV2 syntax](https://core.telegram.org/bots/api#markdownv2-style)), note that to create mentions you can also use the `mention:` syntax like in html:  

```markdown
*bold \*text*
_italic \*text_
__underline__
~strikethrough~
||spoiler||
*bold _italic bold ~italic bold strikethrough ||italic bold strikethrough spoiler||~ __underline italic bold___ bold*
[inline URL](http://www.example.com/)
[inline mention of a user](tg://user?id=123456789)
![👍](tg://emoji?id=5368324170671202286)
\`inline fixed-width code\`
\`\`\`
pre-formatted fixed-width code block
\`\`\`
\`\`\`php
pre-formatted fixed-width code block written in the PHP programming language
\`\`\`

[Mention by username](mention:@danogentili)
[Mention by user id](mention:186785362)
[Mention by user id](tg://user?id=186785362)
[👍](emoji:5368324170671202286)
[👍](tg://emoji?id=5368324170671202286)
```

### Example:

```
$message = ['_' => 'message', 'out' => Bool, 'mentioned' => Bool, 'media_unread' => Bool, 'silent' => Bool, 'post' => Bool, 'from_scheduled' => Bool, 'legacy' => Bool, 'edit_hide' => Bool, 'pinned' => Bool, 'noforwards' => Bool, 'invert_media' => Bool, 'offline' => Bool, 'video_processing_pending' => Bool, 'id' => int, 'from_id' => Peer, 'from_boosts_applied' => int, 'peer_id' => Peer, 'saved_peer_id' => Peer, 'fwd_from' => MessageFwdHeader, 'via_bot_id' => long, 'via_business_bot_id' => long, 'reply_to' => MessageReplyHeader, 'date' => int, 'message' => 'string', 'media' => MessageMedia, 'reply_markup' => ReplyMarkup, 'entities' => [MessageEntity, MessageEntity]parse_mode: 'string', , 'views' => int, 'forwards' => int, 'replies' => MessageReplies, 'edit_date' => int, 'post_author' => 'string', 'grouped_id' => long, 'reactions' => MessageReactions, 'restriction_reason' => [RestrictionReason, RestrictionReason], 'ttl_period' => int, 'quick_reply_shortcut_id' => int, 'effect' => long, 'factcheck' => FactCheck, 'report_delivery_until_date' => int];
```  
