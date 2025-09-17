---
title: "Uploading and downloading files"
description: "MadelineProto provides fully parallelized wrapper methods to upload and download files that support bot API file ids, direct upload by URL and file renaming."
nav_order: 22
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Uploading and downloading files

MadelineProto provides **fully parallelized** wrapper methods to upload and download files that support bot API file ids, direct upload by URL and file renaming.

Maximum file size is of 4 GB.

Example bot: [`downloadRenameBot.php`](https://github.com/danog/downloadRenameBot/blob/main/bot.php) - download files by URL and rename Telegram files using this async parallelized bot!


* [Bot API file IDs](#bot-api-file-ids)
* [Uploading & sending files](#sending-files)
  * [Security notice](#security-notice)
  * [Photos](#photos)
  * [Photos as documents](#photos-as-documents)
  * [Documents](#documents)
  * [GIFs](#gifs)
  * [Videos](#videos)
  * [Music](#music)
  * [Voice](#voice)
  * [Stickers](#stickers)
* [Uploading files](#uploading-files)
* [Reusing uploaded files](#reusing-uploaded-files)
* [Renaming files](#renaming-files)
* [Downloading files](#downloading-files)
  * [Extracting download info](#extracting-download-info)
  * [Getting a download link](#getting-a-download-link)
  * [Downloading profile pictures](#downloading-profile-pictures)
  * [Download to directory](#download-to-directory)
  * [Download to file](#download-to-file)
  * [Download to stream](#download-to-stream)
  * [Download to callback](#download-to-callback)
  * [Download to http-server](#download-to-http-server)
  * [Download to browser](#download-to-browser)
* [Getting progress](#getting-progress)

## Sending files

To send photos and documents to someone, use the [$MadelineProto->messages->sendMedia](https://docs.madelineproto.xyz/API_docs/methods/messages.sendMedia.html) method, click on the link for more info.

All files will be uploaded **asynchronously and in parallel**, 20 chunks at a time for maximum performance (this value can be tweaked in the [settings](https://docs.madelineproto.xyz/docs/SETTINGS.html)).

The required `message` parameter is the caption: it can contain URLs, mentions, bold and italic text, thanks to the `parse_mode` parameter, that enables markdown or HTML parsing.

The `media` parameter contains the file path and other info about the file.

It can contain [lots of various objects](https://docs.madelineproto.xyz/API_docs/types/InputMedia.html), here are the most important:

### Security notice

Be careful when calling methods with user-provided parameters: the upload function may be used to access and send any file.  
To disable automatic uploads by file name (disabled by default), [use the appropriate setting](../PHP/danog/MadelineProto/Settings/Files.html#setallowautomaticuploadbool-allowautomaticupload-self) OR upload files [manually](#reusing-uploaded-files).


### Photos
```php
use danog\MadelineProto\LocalFile;
use danog\MadelineProto\RemoteUrl;
use danog\MadelineProto\BotApiFileId;

use danog\MadelineProto\ParseMode;

$file = new LocalFile('faust.jpg');

// $file = new RemoteUrl('https://example.com/img.jpg');
// ...
// $file can also be a Message, Media, BotApiFileId, ReadableStream object.

$sentMessage = $MadelineProto->sendPhoto(
    peer: '@danogentili',
    file: $file,
    caption: '[This is the caption](https://t.me/MadelineProto)',
    parseMode: ParseMode::MARKDOWN
);
```

Click [here &raquo;](https://docs.madelineproto.xyz/PHP/danog/MadelineProto/API.html#sendPhoto) to see the full list of arguments to set set the self-destruction period of the photo, and many more parameters.  

[An uploadPhoto method is also available to upload a photo without sending it to any chat &raquo;](https://docs.madelineproto.xyz/PHP/danog/MadelineProto/API.html#uploadPhoto)

### Photos as documents
```php
use danog\MadelineProto\LocalFile;
use danog\MadelineProto\RemoteUrl;
use danog\MadelineProto\BotApiFileId;

use danog\MadelineProto\ParseMode;

$file = new LocalFile('faust.jpg');

// $file = new RemoteUrl('https://example.com/img.jpg');
// ...
// $file can also be a Message, Media, BotApiFileId, ReadableStream object.

$sentMessage = $MadelineProto->sendDocumentPhoto(
    peer: '@danogentili',
    file: $file,
    caption: '[This is the caption](https://t.me/MadelineProto)',
    parseMode: ParseMode::MARKDOWN
);
```

Click [here &raquo;](https://docs.madelineproto.xyz/PHP/danog/MadelineProto/API.html#sendDocumentPhoto) to see the full list of arguments to set set the self-destruction period of the photo, and many more parameters.  

[An uploadDocumentPhoto method is also available to upload a document photo without sending it to any chat &raquo;](https://docs.madelineproto.xyz/PHP/danog/MadelineProto/API.html#uploadDocumentPhoto)

### Documents

```php
use danog\MadelineProto\LocalFile;
use danog\MadelineProto\RemoteUrl;
use danog\MadelineProto\BotApiFileId;

use danog\MadelineProto\ParseMode;

$file = new LocalFile('faust.txt');

// $file = new RemoteUrl('https://example.com/file.txt');
// ...
// $file can also be a Message, Media, BotApiFileId, ReadableStream object.

$sentMessage = $MadelineProto->sendDocument(
    peer: '@danogentili',
    file: $file,
    caption: '[This is the caption](https://t.me/MadelineProto)',
    parseMode: ParseMode::MARKDOWN
);
```

Click [here &raquo;](https://docs.madelineproto.xyz/PHP/danog/MadelineProto/API.html#sendDocument) to see the full list of arguments to set set the self-destruction period of the document, and many more parameters.  

To rename files, provide a Message or another already-uploaded Telegram file object to the `file` field.  

[An uploadDocument method is also available to upload a document without sending it to any chat &raquo;](https://docs.madelineproto.xyz/PHP/danog/MadelineProto/API.html#uploadDocument).

### GIFs
```php
use danog\MadelineProto\LocalFile;
use danog\MadelineProto\RemoteUrl;
use danog\MadelineProto\BotApiFileId;

use danog\MadelineProto\ParseMode;

$file = new LocalFile('gif.mp4');

// $file = new RemoteUrl('https://example.com/gif.mp4');
// ...
// $file can also be a Message, Media, BotApiFileId, ReadableStream object.

$sentMessage = $MadelineProto->sendGif(
    peer: '@danogentili',
    file: $file,
    caption: '[This is the caption](https://t.me/MadelineProto)',
    parseMode: ParseMode::MARKDOWN
);
```
Click [here &raquo;](https://docs.madelineproto.xyz/PHP/danog/MadelineProto/API.html#sendGif) to see the full list of arguments to set set the self-destruction period of the document, and many more parameters.  

MadelineProto will **automatically** extract the video's thumbnail, duration, width and height using ffmpeg, if installed.  

[An uploadGif method is also available to upload a gif without sending it to any chat &raquo;](https://docs.madelineproto.xyz/PHP/danog/MadelineProto/API.html#uploadGif)

### Videos

```php
use danog\MadelineProto\LocalFile;
use danog\MadelineProto\RemoteUrl;
use danog\MadelineProto\BotApiFileId;

use danog\MadelineProto\ParseMode;

$file = new LocalFile('video.mp4');

// $file = new RemoteUrl('https://example.com/video.mp4');
// ...
// $file can also be a Message, Media, BotApiFileId, ReadableStream object.

$sentMessage = $MadelineProto->sendVideo(
    peer: '@danogentili',
    file: $file,
    caption: '[This is the caption](https://t.me/MadelineProto)',
    parseMode: ParseMode::MARKDOWN
);
```

Click [here &raquo;](https://docs.madelineproto.xyz/PHP/danog/MadelineProto/API.html#sendVideo) to see the full list of arguments to set set the self-destruction period of the document, send round videos, and many more parameters.  

MadelineProto will **automatically** extract the video's thumbnail, duration, width and height using ffmpeg, if installed.  

[An uploadVideo method is also available to upload a video without sending it to any chat &raquo;](https://docs.madelineproto.xyz/PHP/danog/MadelineProto/API.html#uploadVideo)
### Music

```php
use danog\MadelineProto\LocalFile;
use danog\MadelineProto\RemoteUrl;
use danog\MadelineProto\BotApiFileId;

use danog\MadelineProto\ParseMode;

$file = new LocalFile('song.mp3');

// $file = new RemoteUrl('https://example.com/song.mp3');
// ...
// $file can also be a Message, Media, BotApiFileId, ReadableStream object.

$sentMessage = $MadelineProto->sendAudio(
    peer: '@danogentili',
    file: $file,
    caption: '[This is the caption](https://t.me/MadelineProto)',
    parseMode: ParseMode::MARKDOWN
);
```

Click [here &raquo;](https://docs.madelineproto.xyz/PHP/danog/MadelineProto/API.html#sendAudio) to see the full list of arguments to set set the self-destruction period of the document, and many more parameters.  

MadelineProto will **automatically** extract the music's thumbnail and duration using ffmpeg, if installed.  

[An uploadAudio method is also available to upload an audio without sending it to any chat &raquo;](https://docs.madelineproto.xyz/PHP/danog/MadelineProto/API.html#uploadAudio)

### Voice

```php
use danog\MadelineProto\LocalFile;
use danog\MadelineProto\RemoteUrl;
use danog\MadelineProto\BotApiFileId;

use danog\MadelineProto\ParseMode;

$file = new LocalFile('voice.ogg');

// $file = new RemoteUrl('https://example.com/voice.ogg');
// ...
// $file can also be a Message, Media, BotApiFileId, ReadableStream object.

$sentMessage = $MadelineProto->sendVoice(
    peer: '@danogentili',
    file: $file,
    caption: '[This is the caption](https://t.me/MadelineProto)',
    parseMode: ParseMode::MARKDOWN
);
```

Click [here &raquo;](https://docs.madelineproto.xyz/PHP/danog/MadelineProto/API.html#sendVoice) to see the full list of arguments to set set the self-destruction period of the document, and many more parameters.  

MadelineProto will **automatically** extract the voice message's duration using ffmpeg, if installed.  

[An uploadVoice method is also available to upload a voice message without sending it to any chat &raquo;](https://docs.madelineproto.xyz/PHP/danog/MadelineProto/API.html#uploadVoice)


### Stickers

```php
use danog\MadelineProto\LocalFile;
use danog\MadelineProto\RemoteUrl;
use danog\MadelineProto\BotApiFileId;

use danog\MadelineProto\ParseMode;

$file = new LocalFile('sticker.webp');

// $file = new RemoteUrl('https://example.com/sticker.webp');
// ...
// $file can also be a Message, Media, BotApiFileId, ReadableStream object.

$sentMessage = $MadelineProto->sendSticker(
    peer: '@danogentili',
    file: $file,
    mimeType: 'image/webp',
    caption: '[This is the caption](https://t.me/MadelineProto)',
    parseMode: ParseMode::MARKDOWN
);
```

Click [here &raquo;](https://docs.madelineproto.xyz/PHP/danog/MadelineProto/API.html#sendSticker) to see the full list of arguments to set set the self-destruction period of the document, and many more parameters.  

[An uploadSticker method is also available to upload a sticker without sending it to any chat &raquo;](https://docs.madelineproto.xyz/PHP/danog/MadelineProto/API.html#uploadSticker)


## Uploading files

```php
$MessageMedia = $MadelineProto->messages->uploadMedia([
    'media' => [
        '_' => 'inputMediaUploadedPhoto',
        'file' => 'faust.jpg'
    ],
]);
```

The `file` can be a file name, a URL, or a file uploaded by someone else (can be used to rename files).

You can also only upload a file, without actually sending it to anyone, storing only the file ID for later usage.

All files will be uploaded **asynchronously and in parallel**, 20 chunks at a time for maximum performance (this value can be tweaked in the [settings](https://docs.madelineproto.xyz/docs/SETTINGS.html)).

The [$MadelineProto->messages->uploadMedia](https://docs.madelineproto.xyz/API_docs/methods/messages_uploadMedia.html) function is a reduced version of the [$MadelineProto->messages->sendMedia](https://docs.madelineproto.xyz/API_docs/methods/messages_sendMedia.html), that requires only a `media` parameter, with the media to upload (on normal users, the `peer` field should be populated with `@me` or another value).  

The returned [MessageMedia](https://docs.madelineproto.xyz/API_docs/types/MessageMedia.html) object can then be reused to resend the document using sendMedia.

```php
$sentMessage = $MadelineProto->messages->sendMedia([
    'peer' => '@danogentili',
    'media' => $MessageMedia,
    'message' => '[This is the caption](https://t.me/MadelineProto)',
    'parse_mode' => 'Markdown'
]);
```

`$MessageMedia` can also be a [Message](https://docs.madelineproto.xyz/API_docs/types/Message.html) (the media contained in the message will be sent), an [Update](https://docs.madelineproto.xyz/API_docs/types/Update.html) (the media contained in the message contained in the update will be sent).

## Reusing uploaded files

`$MadelineProto->messages->uploadMedia` and bot API file IDs do not allow you to modify the type of the file to send: however, MadelineProto provides methods that can generate a file object that can be resent with multiple file types.

```php
$inputFile = $MadelineProto->upload('filename.mp4');
```

The file name can also be a URL.  
More optional parameters are available, check the PHPDOC of the method in your IDE.  
You can also upload a file from a stream (this is especially useful, for example, when downloading YouTube videos using `youtube-dl` with `ffmpeg` and [async AMPHP CLI streams](https://github.com/amphp/process)):  

```php
$inputFile = $MadelineProto->uploadFromStream($stream);
```

`$stream` - PHP resource or [async AMPHP stream](https://github.com/amphp/byte-stream).  

More optional parameters are available, check the PHPDOC of the method in your IDE.  
You can also upload files from a callable:

```php
$inputFile = $MadelineProto->uploadFromCallable($callable, $size, $mime);
```

`$callable`:  
The callable must accept two parameters: `int $offset, int $size`  
The callable must return a string with the contest of the file at the specified offset and size.  

More optional parameters are available, check the PHPDOC of the method in your IDE.  

You can also re-use a media received in a message or update, for example in the [event handler](https://docs.madelineproto.xyz/docs/UPDATES.html):  

```php
$inputFile = $update;
$inputFile = $message;
```

---

The generated `$inputFile` can later be reused thusly:

```php
$sentMessage = $MadelineProto->messages->sendMedia([
    'peer' => '@danogentili',
    'media' => [
        '_' => 'inputMediaUploadedDocument',
        'file' => $inputFile,
        'attributes' => [
            ['_' => 'documentAttributeFilename', 'file_name' => 'video.mp4']
        ]
    ],
    'message' => '[This is the caption](https://t.me/MadelineProto)',
    'parse_mode' => 'Markdown'
]);
$sentMessageVideo = $MadelineProto->messages->sendMedia([
    'peer' => '@danogentili',
    'media' => [
        '_' => 'inputMediaUploadedDocument',
        'file' => $inputFile,
        'attributes' => [
            ['_' => 'documentAttributeVideo', 'round_message' => false, 'supports_streaming' => true]
        ]
    ],
    'message' => '[This is the caption](https://t.me/MadelineProto)',
    'parse_mode' => 'Markdown'
]);
```

In this case, we're reusing the same InputFile to send both a document and a video, without uploading the file twice.

The concept is easy: where you would usually provide a file path, simply provide `$inputFile`.

## Renaming files

Files can be renamed by simply providing the `$Update` with the file to the sendMedia method thusly:  

```php
$sentMessage = $MadelineProto->messages->sendMedia([
    'peer' => '@danogentili',
    'media' => [
        '_' => 'inputMediaUploadedDocument',
        'file' => $Update,
        'attributes' => [
            ['_' => 'documentAttributeFilename', 'file_name' => $newName]
        ]
    ],
    'message' => '[This is the caption](https://t.me/MadelineProto)',
    'parse_mode' => 'Markdown'
]);
```

## Downloading files

There are multiple download methods that allow you to download a file to a directory, to a file or to a stream.  

### Extracting download info
```php
$info = $MadelineProto->getDownloadInfo($MessageMedia);
```

`$MessageMedia` can be a [MessageMedia](https://docs.madelineproto.xyz/API_docs/types/MessageMedia.html) object or a bot API file ID.

You can also use [getDownloadLink](#getting-a-download-link) to obtain a direct download link for any file up to 4GB.

* `$info['ext']` - The file extension
* `$info['name']` - The file name, without the extension
* `$info['mime']` - The file mime type
* `$info['size']` - The file size

### Getting a download link

To obtain a direct download link for any Telegram file up to 4GB, simply use `getDownloadLink`, for example:

```php
<?php

if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');

// For bots
$MadelineProto->botLogin('token');

// For users
//$MadelineProto->start();

$botApiFileId = '...';
$fileName = '...';
$fileSize = 123..;
$mimeType = '...';


$link = $MadelineProto->getDownloadLink($botApiFileId, size: $fileSize, name: $fileName, mime: $mimeType);
```

Event handler example with [bound methods](https://docs.madelineproto.xyz/docs/UPDATES.html#bound-methods):

```php
use danog\MadelineProto\SimpleEventHandler;
use danog\MadelineProto\EventHandler\Filter\FilterCommand;
use danog\MadelineProto\EventHandler\Message;
use danog\MadelineProto\EventHandler\SimpleFilter\Incoming;

class MyEventHandler extends SimpleEventHandler
{
    /**
     * Gets a download link for any file up to 4GB!
     */
    #[FilterCommand('dl')]
    public function downloadLink(Incoming&Message $message): void
    {
        $reply = $message->getReply(Message::class);
        if (!$reply?->media) {
            $message->reply("This command must reply to a media message!");
            return;
        }
        $reply->reply("Download link: ".$reply->media->getDownloadLink());
    }
}

MyEventHandler::startAndLoop('bot.madeline')
```

`$botApiFileId` can be a [MessageMedia](https://docs.madelineproto.xyz/API_docs/types/MessageMedia.html) object or a **bot API file ID** (files up to 4GB are supported!).

This method will work automatically only when running via web (apache/php-fpm).  

The generated download `$link` will point to your own server, and the link will stream files directly to the browser (**no temporary files will be created**, **0** disk space will be used).  

#### Getting a download link (CLI bots)

**Only if running via CLI** (or if URL rewriting is enabled on web), a second parameter must be provided with a URL to a download script hosted on a php-fpm/apache instance on the same machine:

```php
<?php

if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');

// For bots
$MadelineProto->botLogin('token');

// For users
//$MadelineProto->start();

$botApiFileId = '...';
$fileName = '...';
$fileSize = 123..;
$mimeType = '...';


$link = $MadelineProto->getDownloadLink($botApiFileId, 'https://yourhost.com/dl.php', size: $fileSize, name: $fileName, mime: $mimeType);
```

Event handler example with [bound methods](https://docs.madelineproto.xyz/docs/UPDATES.html#bound-methods):

```php
use danog\MadelineProto\SimpleEventHandler;
use danog\MadelineProto\EventHandler\Filter\FilterCommand;
use danog\MadelineProto\EventHandler\Message;
use danog\MadelineProto\EventHandler\SimpleFilter\Incoming;

class MyEventHandler extends SimpleEventHandler
{
    /**
     * Gets a download link for any file up to 4GB!
     */
    #[FilterCommand('dl')]
    public function downloadLink(Incoming&Message $message): void
    {
        $reply = $message->getReply(Message::class);
        if (!$reply?->media) {
            $message->reply("This command must reply to a media message!");
            return;
        }
        $reply->reply("Download link: ".$reply->media->getDownloadLink('https://yourhost.com/dl.php'));
    }
}

MyEventHandler::startAndLoop('bot.madeline')
```

You can also pass your custom download link in the [Files settings, instead](https://docs.madelineproto.xyz/docs/FILES.html).  

The dl.php script must have the following content:

```php
<?php

if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

\danog\MadelineProto\API::downloadServer('session.madeline');
```

Note that `session.madeline` must be logged into exactly the same user/bot used by the CLI userbot/bot.  

To login the first time, simple open `dl.php?login=1` in your browser: if the session is not logged in, a login prompt will be shown, otherwise the user/bot ID will be displayed.  

The link will stream files directly to the browser (**no temporary files will be created**, **0** disk space will be used).  

### Downloading profile pictures
```php
$info = $MadelineProto->getPropicInfo($Update);
```

`$Update` can be a [Message](https://docs.madelineproto.xyz/API_docs/types/Message.html) object, an [Update](https://docs.madelineproto.xyz/API_docs/types/Update.html), or any value supported by [getInfo](https://docs.madelineproto.xyz/getInfo.html).  
The result will be a [Photo](https://docs.madelineproto.xyz/PHP/danog/MadelineProto/EventHandler/Media/Photo.html) object.  

### Download to directory
```php
$output_file_name = $MadelineProto->downloadToDir($MessageMedia, '/tmp/');
```

This downloads the given file to `/tmp`, and returns the full generated file path.  

**Note**: if downloading files that will be re-downloaded by the user, use [downloadToBrowser](#download-to-browser), instead: [downloadToBrowser](#download-to-browser) will avoid the creation of temporary files, streaming the file directly to the user.  

You can also use [getDownloadLink](#getting-a-download-link) to obtain a direct download link for any file up to 4GB.  

`$MessageMedia` can be either a [Message](https://docs.madelineproto.xyz/API_docs/types/Message.html), an [Update](https://docs.madelineproto.xyz/API_docs/types/Update.html), a [MessageMedia](https://docs.madelineproto.xyz/API_docs/types/MessageMedia.html) object, or a bot API file ID.

### Download to file
```php
$output_file_name = $MadelineProto->downloadToFile($MessageMedia, '/tmp/myname.mp4');
```

**Note**: if downloading files that will be re-downloaded by the user, use [downloadToBrowser](#download-to-browser), instead: [downloadToBrowser](#download-to-browser) will avoid the creation of temporary files, streaming the file directly to the user.  

You can also use [getDownloadLink](#getting-a-download-link) to obtain a direct download link for any file up to 4GB.  

This downloads the given file to `/tmp/myname.mp4`, and returns the full file path.

`$MessageMedia`can be either a [Message](https://docs.madelineproto.xyz/API_docs/types/Message.html), an [Update](https://docs.madelineproto.xyz/API_docs/types/Update.html), a [MessageMedia](https://docs.madelineproto.xyz/API_docs/types/MessageMedia.html) object, or a bot API file ID.

### Download to stream
```php
$MadelineProto->downloadToStream($MessageMedia, $stream);
```

This downloads the given file to the given resource or [async AMPHP stream](https://github.com/amphp/byte-stream), the latter is especially useful for building an async HTTP file server with [http-server](https://github.com/amphp/http-server).

`$MessageMedia`can be either a [Message](https://docs.madelineproto.xyz/API_docs/types/Message.html), an [Update](https://docs.madelineproto.xyz/API_docs/types/Update.html), a [MessageMedia](https://docs.madelineproto.xyz/API_docs/types/MessageMedia.html) object, or a bot API file ID.


You can also use `downloadToReturnedStream`, which returns an amphp `ReadableStream`, instead:

```php
$stream = $MadelineProto->downloadToReturnedStream($MessageMedia);
```

### Download to callback
```php
$MadelineProto->downloadToCallable($MessageMedia, $callable);
```

This downloads the given file to the callable.
The callable must accept two parameters: `string $payload, int $offset`
The callable will be called (possibly out of order, depending on the value of the `$seekable` (see PHPDOC)).
The callable should return the number of written bytes.  

`$MessageMedia`can be either a [Message](https://docs.madelineproto.xyz/API_docs/types/Message.html), an [Update](https://docs.madelineproto.xyz/API_docs/types/Update.html), a [MessageMedia](https://docs.madelineproto.xyz/API_docs/types/MessageMedia.html) object, or a bot API file ID.


### Download to http-server
```php
$MadelineProto->downloadToResponse($MessageMedia, $request, $cb);
```

This downloads the given file, replying to the specified [async http-server](https://amphp.org/http-server) request.  
Automatically supports HEAD requests and content-ranges for parallel and resumed downloads.  

`$MessageMedia` can be either a [Message](https://docs.madelineproto.xyz/API_docs/types/Message.html), an [Update](https://docs.madelineproto.xyz/API_docs/types/Update.html), a [MessageMedia](https://docs.madelineproto.xyz/API_docs/types/MessageMedia.html) object, or a bot API file ID.

`$request` is the [Request](https://amphp.org/http-server/classes/request) object returned by [http-server](https://amphp.org/http-server).

`$cb` is an optional parameter can be a callback for download progress, but it shouldn't be used, the new [FileCallback](#getting-progress) should be used instead



### Download to browser
```php
$MadelineProto->downloadToBrowser($MessageMedia, $cb);
```

You can also use [getDownloadLink](#getting-a-download-link) to obtain a direct download link for any file up to 4GB.  

This downloads the given file to the browser, sending also information about the file's type and size.
Automatically supports HEAD requests and content-ranges for parallel and resumed downloads.  

`$MessageMedia` can be either a [Message](https://docs.madelineproto.xyz/API_docs/types/Message.html), an [Update](https://docs.madelineproto.xyz/API_docs/types/Update.html), a [MessageMedia](https://docs.madelineproto.xyz/API_docs/types/MessageMedia.html) object, or a bot API file ID.

`$cb` is an optional parameter can be a callback for download progress, but it shouldn't be used, the new [FileCallback](#getting-progress) should be used instead


## Getting progress

To get the upload/download progress in real-time, use the `\danog\MadelineProto\FileCallback` class:

```php
$peer = '@danogentili';
$sentMessage = $MadelineProto->messages->sendMedia([
    'peer' => $peer,
    'media' => [
        '_' => 'inputMediaUploadedDocument',
        'file' => new \danog\MadelineProto\FileCallback(
            'video.mp4',
            function ($progress, $speed, $time) use ($MadelineProto, $peer) {
                try {
                    $MadelineProto->messages->sendMessage(['peer' => $peer, 'message' => "Upload progress: $progress%\nSpeed: $speed mbps\nTime elapsed since start: $time"]);
                } catch (\Throwable $e) {}
            }
        ),
        'attributes' => [
            ['_' => 'documentAttributeVideo', 'round_message' => false, 'supports_streaming' => true]
        ]
    ],
    'message' => '[This is the caption](https://t.me/MadelineProto)',
    'parse_mode' => 'Markdown'
]);

$output_file_name = $MadelineProto->downloadToFile(
    $sentMessage,
    new \danog\MadelineProto\FileCallback(
        '/tmp/myname.mp4',
        function ($progress, $speed, $time) use ($MadelineProto, $peer) {
            try {
                $MadelineProto->messages->sendMessage(['peer' => $peer, 'message' => "Download progress: $progress%\nSpeed: $speed mbps\nTime elapsed since start: $time"]);
            } catch (\Throwable $e) {}
        }
    )
);
```

This will send the file `video.mp4` to [@danogentili](https://t.me/danogentili): while uploading, he will receive progress messages `Upload progress: 24%` until the upload is complete; while downloading, he will receive progress messages `Download progress: 34%` until the download is complete.

You can also add two more parameters `$speed, $time` to the signature of the method to get a partial upload speed in mbps, along with the time elapsed since the start of the download.

A FileCallback object can be provided to `uploadMedia`, `sendMedia`, `uploadProfilePicture`, `upload`, `upload_encrypted`, `download_to_*`: the first parameter to its constructor must be the file path/object that is usually accepted by the function, the second must be a callable function or object.

You can also write your own callback class, just implement `\danog\MadelineProto\FileCallbackInterface`:  
```php
class MyCallback implements \danog\MadelineProto\FileCallbackInterface
{
    private $file;
    private $peer;
    private $MadelineProto;
    public function __construct($file, $peer, $MadelineProto)
    {
        $this->file = $file;
        $this->peer = $peer;
        $this->MadelineProto = $MadelineProto;
    }
    public function getFile()
    {
        return $this->file;
    }
    public function __invoke($progress, $speed, $time)
    {
        $this->MadelineProto->messages->sendMessage(['peer' => $this->peer, 'message' => 'Progress: '.$progress.'%']);
    }
}
$peer = '@danogentili';
$sentMessage = $MadelineProto->messages->sendMedia([
    'peer' => $peer,
    'media' => [
        '_' => 'inputMediaUploadedDocument',
        'file' => new MyCallback('video.mp4', $peer, $MadelineProto),
        'attributes' => [
            ['_' => 'documentAttributeVideo', 'round_message' => false, 'supports_streaming' => true]
        ]
    ],
    'message' => '[This is the caption](https://t.me/MadelineProto)',
    'parse_mode' => 'Markdown'
]);

$output_file_name = $MadelineProto->downloadToFile(
    $sentMessage,
    new MyCallback('/tmp/myname.mp4', $peer, $MadelineProto)
);
```


## Bot API file IDs

`$MessageMedia` can even be a bot API file ID, generated by the bot API, or by MadelineProto:

Actual MessageMedia objects can also be converted to bot API file IDs like this:

```php
$botAPI_file = $MadelineProto->MTProtoToBotAPI($MessageMedia);
```

`$botAPI_file` now contains a [bot API message](https://core.telegram.org/bots/api#message), to extract the file ID from it use the following code:

```php
foreach (['audio', 'document', 'photo', 'sticker', 'video', 'voice', 'video_note'] as $type) {
    if (isset($botAPI_file[$type]) && is_array($botAPI_file[$type])) {
        $method = $type;
    }
}
$result['file_type'] = $method;
if ($result['file_type'] == 'photo') {
    $result['file_size'] = $botAPI_file[$method][0]['file_size'];
    if (isset($botAPI_file[$method][0]['file_name'])) {
        $result['file_name'] = $botAPI_file[$method][0]['file_name'];
        $result['file_id'] = $botAPI_file[$method][0]['file_id'];
    }
} else {
    if (isset($botAPI_file[$method]['file_name'])) {
        $result['file_name'] = $botAPI_file[$method]['file_name'];
    }
    if (isset($botAPI_file[$method]['file_size'])) {
        $result['file_size'] = $botAPI_file[$method]['file_size'];
    }
    if (isset($botAPI_file[$method]['mime_type'])) {
        $result['mime_type'] = $botAPI_file[$method]['mime_type'];
    }
    $result['file_id'] = $botAPI_file[$method]['file_id'];
}
if (!isset($result['mime_type'])) {
    $result['mime_type'] = 'application/octet-stream';
}
if (!isset($result['file_name'])) {
    $result['file_name'] = $result['file_id'].($method === 'sticker' ? '.webp' : '');
}
```

* `$result['file_id']` - Bot API file ID
* `$result['mime_type']` - Mime type
* `$result['file_type']` - File type: voice, video, video_note (round video), music, video, photo, sticker or document
* `$result['file_size']` - File size
* `$result['file_name']` - File name

<a href="https://docs.madelineproto.xyz/docs/CHAT_INFO.html">Next section</a>