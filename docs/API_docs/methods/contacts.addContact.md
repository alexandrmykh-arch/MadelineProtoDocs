---
title: "contacts.addContact"
description: "Add an existing telegram user as contact."
grand_parent: "Telegram RPC API"
parent: "Methods"
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
redirect_from: /API_docs/methods/contacts_addContact.html
---
# Method: contacts.addContact
[Back to methods index](index.html)



Add an existing telegram user as contact.

Use [contacts.importContacts](../methods/contacts.importContacts.html) to add contacts by phone number, without knowing their Telegram ID.

### Parameters:

| Name     |    Type       | Description | Required |
|----------|---------------|-------------|----------|
|add\_phone\_privacy\_exception|[Bool](/API_docs/types/Bool.html) | Allow the other user to see our phone number? | Optional|
|id|[Username, chat ID, Update, Message or InputUser](/API_docs/types/InputUser.html) | Telegram ID of the other user | Optional|
|first\_name|[string](/API_docs/types/string.html) | First name | Optional|
|last\_name|[string](/API_docs/types/string.html) | Last name | Optional|
|phone|[string](/API_docs/types/string.html) | User's phone number, may be omitted to simply add the user to the contact list, without a phone number. | Optional|


### Return type: [Updates](/API_docs/types/Updates.html)

### Can users use this method: **YES**


### Can bots use this method: **NO**


### Can bots use this method over a business connection with the `businessConnectionId` flag: **NO**


### MadelineProto Example ([now async for huge speed and parallelism!](https://docs.madelineproto.xyz/docs/ASYNC.html)):


```php
if (!file_exists('madeline.php')) {
    copy('https://phar.madelineproto.xyz/madeline.php', 'madeline.php');
}
include 'madeline.php';

$MadelineProto = new \danog\MadelineProto\API('session.madeline');
$MadelineProto->start();

$Updates = $MadelineProto->contacts->addContact(add_phone_privacy_exception: $Bool, id: $InputUser, first_name: 'string', last_name: 'string', phone: 'string', );
```

