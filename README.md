# Telegram Bot API errors

## Introduction
This is a non-official list of actual errors you can encounter while developing your bot using the Telegram Bot API.

The meaning, explanations, codes and other stuff in these errors may change at any given time, so don't trust too much on this list and use your common sense.

If you want to contribute, ensure to include: 
- The actual json output
- Optional textual description
- Whether there is interaction needed from the developer
- What method did create the error

## The error list

This is the actual list that has been composed so far. Feel free to add more.

| JSON         | Human Description| Action needed?    | Methods raising |
|--------------|------------------|-------------------|:---------------:|
|[Unauthorized](json/unauthorized.json)|Bot token is incorrect|Correct your bot token and try again|any|
|[Bad Request: chat not found](json/bad-request-chat-not-found.json )|||any|
|[Bad request: user not found](json/bad-request-user-not-found.json)|User_id is incorrect|Correct user_id|any|
|[Forbidden: user is deactivated](json/forbidden-user-is-deactivated.json)|||SendMessage<br />any(?)|
|[Forbidden: bot was kicked](json/forbidden-bot-was-kicked.json)|Bot was kicked|Delete chat_id on your side|SendMessage|
|[Forbidden: bot blocked by user](json/forbidden-bot-blocked-by-user.json)|||any|
|[Forbidden: bot can't send messages to bots](json/forbidden-bot-cant-send-messages-to-bots.json)|You tried to send a message to another bot. This is not possible||sendMessage|
|[Too many requests](json/too-many-requests.json)|You are hitting the API limit, [more information here](https://core.telegram.org/bots/faq#my-bot-is-hitting-limits-how-do-i-avoid-this)||SendMessage|
|[Bad request: Group migrated to supergroup](json/bad-request-group-chat-migrated.json)||SendMessage|
|[Bad request: Invalid file id](json/bad-request-invalid-file-id.json)| The file id you are trying to retrieve doesn't exist|Try to call getFile before downloading|GetFile|
|[Bad request: Message not modified](json/bad-request-message-not-modified.json)|||EditMessageText|
|[Conflict: Terminated by other long poll](json/conflicted-terminated-by-other-long-poll.json)|You have already set up a webhook and are trying to get the updates via getUpdates|Do not use getUpdates|getUpdates|
|[Bad request: Wrong parameter action in request](json/bad-request-wrong-parameter-action-in-request.json)|||sendChatAction|
