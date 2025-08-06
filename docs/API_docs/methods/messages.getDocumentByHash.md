---
title: "messages.getDocumentByHash"
description: "Get a document by its SHA256 hash, mainly used for gifs"
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/messages_getDocumentByHash.html
---
# Method: messages.getDocumentByHash
[Back to methods index](index.html)



Get a document by its SHA256 hash, mainly used for gifs

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|sha256|[bytes](/API_docs/types/bytes.html) | SHA256 of file | Yes|
|size|[long](/API_docs/types/long.html) | Size of the file in bytes | Yes|
|mime\_type|[string](/API_docs/types/string.html) | Mime type | Optional|


### Return type: [Document](/API_docs/types/Document.html)

### Can users use this method: **YES**


### Can bots use this method: **YES**


### Can bots use this method over a business connection with the `businessConnectionId` flag: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$Document = $MadelineProto->messages->getDocumentByHash(sha256: 'bytes', size: $long, mime_type: 'string', );
```

