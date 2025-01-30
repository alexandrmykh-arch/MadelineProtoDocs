---
title: "messageEntityBlockquote"
description: "Message entity representing a block quote."
nav_exclude: true
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: messageEntityBlockquote  
[Back to constructors index](/API_docs/constructors/index.html)



Message entity representing a block quote.

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|collapsed|[Bool](/API_docs/types/Bool.html) | Optional|Whether the quote is collapsed by default.|
|offset|[int](/API_docs/types/int.html) | Yes|Offset of message entity within message (in [UTF-16 code units](https://core.telegram.org/api/entities#entity-length))|
|length|[int](/API_docs/types/int.html) | Yes|Length of message entity within message (in [UTF-16 code units](https://core.telegram.org/api/entities#entity-length))|



### Type: [MessageEntity](/API_docs/types/MessageEntity.html)


### Example:

```
$messageEntityBlockquote = ['_' => 'messageEntityBlockquote', 'collapsed' => Bool, 'offset' => int, 'length' => int];
```  
