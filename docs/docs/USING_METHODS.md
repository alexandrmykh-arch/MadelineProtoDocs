---
title: "Using methods"
description: "There are simplifications for many, if not all of, these methods."
nav_order: 31
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Using methods

There are simplifications for many, if not all of, these methods.

A list of all of the methods that can be called with MadelineProto can be found here: [here (layer 211)](https://docs.madelineproto.xyz/API_docs/).

 [Now fully async!](https://docs.madelineproto.xyz/docs/ASYNC.html)

* [Named arguments](#named-arguments)
* [Peers](#peers)
* [Files](https://docs.madelineproto.xyz/docs/FILES.html)
* [Secret chats](#secret-chats)
* [Entities (Markdown & HTML)](#entities)
* [reply_markup (keyboards & inline keyboards)](#reply_markup)
* [bot API objects](#bot-api-objects)
* [No result](#no-result)
* [Multiple method calls](#multiple-method-calls)
* [Cancellation](#cancellation)
* [FULL API Documentation with descriptions](https://docs.madelineproto.xyz/API_docs/methods/)

## Named arguments

You must use named arguments instead of arrays to provide method arguments, which allows for much cleaner syntax:

```php
$MadelineProto->messages->sendMessage(peer: '@danogentili', message: 'Testing MadelineProto...');
```

## Peers
[Full example](https://github.com/danog/MadelineProto/blob/v8/bot.php)

If an object of type User, InputUser, Chat, InputChannel, Peer or InputPeer must be provided as a parameter to a method, you can substitute it with the user/group/channel's username (`@username`), bot API id (`-1029449`, `1249421`, `-100412412901`), or update.  

```php
$MadelineProto->messages->sendMessage(peer: '@danogentili', message: 'Testing MadelineProto...');
```


## Secret chats
[Full example](https://github.com/danog/MadelineProto/blob/v8/examples/secret_bot.php)
If an object of type InputSecretChat must be provided as a parameter to a method, you can substitute it with the secret chat's id, the updateNewEncrypted message or the decryptedMessage:

```php
$MadelineProto->messages->sendEncrypted(peer: $update, message: ['_' => 'decryptedMessage', 'ttl' => 0, 'message' => 'Hi']);
```


## Entities
[Full example](https://github.com/danog/MadelineProto/blob/v8/tests/testing.php)
Methods that allow sending message entities ([messages.sendMessage](http://docs.madelineproto.xyz/API_docs/methods/messages_sendMessage.html) for example) also have an additional `parse_mode` parameter that enables or disables html/markdown parsing of the message to be sent.

```php
$MadelineProto->messages->sendMessage(peer: '@danogentili', message: '[Testing Markdown in MadelineProto](https://docs.madelineproto.xyz)', parse_mode:  'Markdown');
$MadelineProto->messages->sendMessage(peer: '@danogentili', message: '<a href="https://docs.madelineproto.xyz">Testing HTML in MadelineProto</a>', parse_mode:  'HTML');
```



## reply_markup
reply_markup accepts bot API reply markup objects as well as MTProto ones.

```php
$bot_API_markup = ['inline_keyboard' => 
    [
        [
            ['text' => 'MadelineProto docs', 'url' => 'https://docs.madelineproto.xyz'],
            ['text' => 'MadelineProto channel', 'url' => 'https://t.me/MadelineProto']
        ]
    ]
];
$MadelineProto->messages->sendMessage(peer: '@danogentili', message: 'lel', reply_markup: $bot_API_markup);
```


## Bot API objects
To convert the results of methods to bot API objects you can use the MTProtoToBotAPI method.

```php
$bot_API_object = $MadelineProto->MTProtoToBotAPI($MadelineProto->messages->sendMessage(peer: '@danogentili', message: 'lel'));
```

MadelineProto also [supports bot API file IDs when working with files](FILES.html)


## No result

See [ignored async](https://docs.madelineproto.xyz/docs/ASYNC.html#ignored-async).  

## Multiple method calls

See [multiple async](https://docs.madelineproto.xyz/docs/ASYNC.html#multiple-async).  

## Cancellation

See [cancellation &raquo;](https://docs.madelineproto.xyz/docs/ASYNC.html#cancellation).  

<a href="https://docs.madelineproto.xyz/docs/CONTRIB.html">Next section</a>