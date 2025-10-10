---
title: "messages.sendMedia"
description: "Send a media"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_sendMedia.html
---
# Method: messages.sendMedia
[Back to methods index](index.html)



Send a media

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|silent|[Bool](/API_docs/types/Bool.html) | Send message silently (no notification should be triggered) | Optional|
|background|[Bool](/API_docs/types/Bool.html) | Send message in background | Optional|
|clear\_draft|[Bool](/API_docs/types/Bool.html) | Clear the draft | Optional|
|noforwards|[Bool](/API_docs/types/Bool.html) | Only for bots, disallows forwarding and saving of the messages, even if the destination chat doesn't have [content protection](https://telegram.org/blog/protected-content-delete-by-date-and-more) enabled | Optional|
|update\_stickersets\_order|[Bool](/API_docs/types/Bool.html) | Whether to move used stickersets to top, [see here for more info on this flag »](https://core.telegram.org/api/stickers#recent-stickersets) | Optional|
|invert\_media|[Bool](/API_docs/types/Bool.html) | If set, any eventual webpage preview will be shown on top of the message instead of at the bottom. | Optional|
|allow\_paid\_floodskip|[Bool](/API_docs/types/Bool.html) | Bots only: if set, allows sending up to 1000 messages per second, ignoring [broadcasting limits](https://core.telegram.org/bots/faq#how-can-i-message-all-of-my-bot-39s-subscribers-at-once) for a fee of 0.1 Telegram Stars per message. The relevant Stars will be withdrawn from the bot's balance. | Optional|
|peer|[Username, chat ID, Update, Message or InputPeer](/API_docs/types/InputPeer.html) | Destination | Optional|
|reply\_to|[InputReplyTo](/API_docs/types/InputReplyTo.html) | If set, indicates that the message should be sent in reply to the specified message or story. | Optional|
|media|[MessageMedia, Update, Message or InputMedia](/API_docs/types/InputMedia.html) | Attached media | Optional|
|message|[string](/API_docs/types/string.html) | Caption | Optional|
|reply\_markup|[ReplyMarkup](/API_docs/types/ReplyMarkup.html) | Reply markup for bot keyboards | Optional|
|entities|Array of [MessageEntity](/API_docs/types/MessageEntity.html) | Message [entities](https://core.telegram.org/api/entities) for styled text | Optional|
|parse\_mode| [string](/API_docs/types/string.html) | Whether to parse HTML or Markdown markup in the message| Optional |
|schedule\_date|[int](/API_docs/types/int.html) | Scheduled message date for [scheduled messages](https://core.telegram.org/api/scheduled-messages) | Optional|
|send\_as|[Username, chat ID, Update, Message or InputPeer](/API_docs/types/InputPeer.html) | Send this message as the specified peer | Optional|
|quick\_reply\_shortcut|[InputQuickReplyShortcut](/API_docs/types/InputQuickReplyShortcut.html) | Add the message to the specified [quick reply shortcut »](https://core.telegram.org/api/business#quick-reply-shortcuts), instead. | Optional|
|effect|[long](/API_docs/types/long.html) | Specifies a [message effect »](https://core.telegram.org/api/effects) to use for the message. | Optional|
|allow\_paid\_stars|[long](/API_docs/types/long.html) | For [paid messages »](https://core.telegram.org/api/paid-messages), specifies the amount of [Telegram Stars](https://core.telegram.org/api/stars) the user has agreed to pay in order to send the message. | Optional|
|suggested\_post|[SuggestedPost](/API_docs/types/SuggestedPost.html) | Used to [suggest a post to a channel, see here »](https://core.telegram.org/api/suggested-posts) for more info on the full flow. | Optional|


### Return type: [Updates](/API_docs/types/Updates.html)

### Can users use this method: **YES**


### Can bots use this method: **YES**


### Can bots use this method over a business connection with the `businessConnectionId` flag: **YES**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$Updates = $MadelineProto->messages->sendMedia(silent: $Bool, background: $Bool, clear_draft: $Bool, noforwards: $Bool, update_stickersets_order: $Bool, invert_media: $Bool, allow_paid_floodskip: $Bool, peer: $InputPeer, reply_to: $InputReplyTo, media: $InputMedia, message: 'string', reply_markup: $ReplyMarkup, entities: [$MessageEntity, $MessageEntity], parse_mode: 'string', schedule_date: $int, send_as: $InputPeer, quick_reply_shortcut: $InputQuickReplyShortcut, effect: $long, allow_paid_stars: $long, suggested_post: $SuggestedPost, );
```


## Usage of reply_markup

You can provide bot API reply_markup objects here.  



## Return value 

If the length of the provided message is bigger than 4096, the message will be split in chunks and the method will be called multiple times, with the same parameters (except for the message), and an array of [Updates](../types/Updates.html) will be returned instead.



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

