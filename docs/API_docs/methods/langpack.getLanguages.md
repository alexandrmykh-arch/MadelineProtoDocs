---
title: "langpack.getLanguages"
description: "Get information about all languages in a localization pack"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/langpack_getLanguages.html
---
# Method: langpack.getLanguages
[Back to methods index](index.html)



Get information about all languages in a localization pack

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|lang\_pack|[string](/API_docs/types/string.html) | Platform identifier (i.e. `android`, `tdesktop`, etc). | Optional|


### Return type: [Vector\_of\_LangPackLanguage](/API_docs/types/LangPackLanguage.html)

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

$Vector_of_LangPackLanguage = $MadelineProto->langpack->getLanguages(lang_pack: 'string', );
```

