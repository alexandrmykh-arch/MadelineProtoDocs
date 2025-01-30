---
title: "stickers.createStickerSet"
description: "Create a stickerset."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/stickers_createStickerSet.html
---
# Method: stickers.createStickerSet
[Back to methods index](index.html)



Create a stickerset.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|masks|[Bool](/API_docs/types/Bool.html) | Whether this is a mask stickerset | Optional|
|emojis|[Bool](/API_docs/types/Bool.html) | Whether this is a [custom emoji](https://core.telegram.org/api/custom-emoji) stickerset. | Optional|
|text\_color|[Bool](/API_docs/types/Bool.html) | Whether the color of TGS custom emojis contained in this set should be changed to the text color when used in messages, the accent color if used as emoji status, white on chat photos, or another appropriate color based on context. For custom emoji stickersets only. | Optional|
|user\_id|[Username, chat ID, Update, Message or InputUser](/API_docs/types/InputUser.html) | Stickerset owner | Optional|
|title|[string](/API_docs/types/string.html) | Stickerset name, `1-64` chars | Optional|
|short\_name|[string](/API_docs/types/string.html) | Short name of sticker set, to be used in [sticker deep links »](https://core.telegram.org/api/links#stickerset-links). Can contain only english letters, digits and underscores. Must begin with a letter, can't contain consecutive underscores and, **if called by a bot**, must end in `"_by_<bot_username>"`. `<bot_username>` is case insensitive. 1-64 characters. | Optional|
|thumb|[MessageMedia, Update, Message or InputDocument](/API_docs/types/InputDocument.html) | Thumbnail | Optional|
|stickers|Array of [InputStickerSetItem](/API_docs/types/InputStickerSetItem.html) | Stickers | Yes|
|software|[string](/API_docs/types/string.html) | Used when [importing stickers using the sticker import SDKs](https://core.telegram.org/import-stickers), specifies the name of the software that created the stickers | Optional|


### Return type: [messages.StickerSet](/API_docs/types/messages.StickerSet.html)

### Can userbots use this method: **YES**

### Can bots use this method: **YES**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$messages_StickerSet = $MadelineProto->stickers->createStickerSet(masks: $Bool, emojis: $Bool, text_color: $Bool, user_id: $InputUser, title: 'string', short_name: 'string', thumb: $InputDocument, stickers: [$InputStickerSetItem, $InputStickerSetItem], software: 'string', );
```

