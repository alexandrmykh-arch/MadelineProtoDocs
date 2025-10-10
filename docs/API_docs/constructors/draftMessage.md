---
title: "draftMessage"
description: "Represents a message draft."
nav_exclude: true
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: draftMessage  
[Back to constructors index](/API_docs/constructors/index.html)



Represents a message [draft](https://core.telegram.org/api/drafts).

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|no\_webpage|[Bool](/API_docs/types/Bool.html) | Optional|Whether no webpage preview will be generated|
|invert\_media|[Bool](/API_docs/types/Bool.html) | Optional|If set, any eventual webpage preview will be shown on top of the message instead of at the bottom.|
|reply\_to|[InputReplyTo](/API_docs/types/InputReplyTo.html) | Optional|If set, indicates that the message should be sent in reply to the specified message or story.|
|message|[string](/API_docs/types/string.html) | Yes|The draft|
|entities|Array of [MessageEntity](/API_docs/types/MessageEntity.html) | Optional|Message [entities](https://core.telegram.org/api/entities) for styled text.|
|parse\_mode| [string](/API_docs/types/string.html) | Whether to parse HTML or Markdown markup in the message| Optional |
|media|[InputMedia](/API_docs/types/InputMedia.html) | Optional|Media.|
|date|[int](/API_docs/types/int.html) | Yes|Date of last update of the draft.|
|effect|[long](/API_docs/types/long.html) | Optional|A [message effect that should be played as specified here »](https://core.telegram.org/api/effects).|
|suggested\_post|[SuggestedPost](/API_docs/types/SuggestedPost.html) | Optional|Used to [suggest a post to a channel, see here »](https://core.telegram.org/api/suggested-posts) for more info on the full flow.|



### Type: [DraftMessage](/API_docs/types/DraftMessage.html)



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
$draftMessage = ['_' => 'draftMessage', 'no_webpage' => Bool, 'invert_media' => Bool, 'reply_to' => InputReplyTo, 'message' => 'string', 'entities' => [MessageEntity, MessageEntity]parse_mode: 'string', , 'media' => InputMedia, 'date' => int, 'effect' => long, 'suggested_post' => SuggestedPost];
```  
