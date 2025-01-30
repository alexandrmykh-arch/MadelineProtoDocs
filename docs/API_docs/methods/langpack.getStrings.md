---
title: "langpack.getStrings"
description: "Get strings from a language pack"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/langpack_getStrings.html
---
# Method: langpack.getStrings
[Back to methods index](index.html)



Get strings from a language pack

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|lang\_pack|[string](/API_docs/types/string.html) | Platform identifier (i.e. `android`, `tdesktop`, etc). | Optional|
|lang\_code|[string](/API_docs/types/string.html) | Either an ISO 639-1 language code or a language pack name obtained from a [language pack link](https://core.telegram.org/api/links#language-pack-links). | Optional|
|keys|Array of [string](/API_docs/types/string.html) | Strings to get | Yes|


### Return type: [Vector\_of\_LangPackString](/API_docs/types/LangPackString.html)

### Can userbots use this method: **YES**

### Can bots use this method: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$Vector_of_LangPackString = $MadelineProto->langpack->getStrings(lang_pack: 'string', lang_code: 'string', keys: ['string', 'string'], );
```

