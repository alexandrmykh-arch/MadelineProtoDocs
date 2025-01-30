---
title: "inputMediaInvoice"
description: "Generated invoice of a bot payment"
nav_exclude: true
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: inputMediaInvoice  
[Back to constructors index](/API_docs/constructors/index.html)



Generated invoice of a [bot payment](https://core.telegram.org/bots/payments)

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|title|[string](/API_docs/types/string.html) | Yes|Product name, 1-32 characters|
|description|[string](/API_docs/types/string.html) | Yes|Product description, 1-255 characters|
|photo|[InputWebDocument](/API_docs/types/InputWebDocument.html) | Optional|URL of the product photo for the invoice. Can be a photo of the goods or a marketing image for a service. People like it better when they see what they are paying for.|
|invoice|[Invoice](/API_docs/types/Invoice.html) | Yes|The actual invoice|
|payload|[bytes](/API_docs/types/bytes.html) | Yes|Bot-defined invoice payload, 1-128 bytes. This will not be displayed to the user, use for your internal processes.|
|provider|[string](/API_docs/types/string.html) | Optional|Payments provider token, obtained via [Botfather](https://t.me/botfather)|
|provider\_data|[DataJSON](/API_docs/types/DataJSON.html) | Yes|JSON-encoded data about the invoice, which will be shared with the payment provider. A detailed description of required fields should be provided by the payment provider.|
|start\_param|[string](/API_docs/types/string.html) | Optional|Unique [bot deep links start parameter](https://core.telegram.org/api/links#bot-links). If present, forwarded copies of the sent message will have a URL button with a [deep link](https://core.telegram.org/api/links#bot-links) to the bot (instead of a Pay button), with the value used as the start parameter. If absent, forwarded copies of the sent message will have a Pay button, allowing multiple users to pay directly from the forwarded message, using the same invoice.|
|extended\_media|[MessageMedia, Message, Update or InputMedia](/API_docs/types/InputMedia.html) | Optional|Deprecated|



### Type: [InputMedia](/API_docs/types/InputMedia.html)


### Example:

```
$inputMediaInvoice = ['_' => 'inputMediaInvoice', 'title' => 'string', 'description' => 'string', 'photo' => InputWebDocument, 'invoice' => Invoice, 'payload' => 'bytes', 'provider' => 'string', 'provider_data' => DataJSON, 'start_param' => 'string', 'extended_media' => InputMedia];
```  
