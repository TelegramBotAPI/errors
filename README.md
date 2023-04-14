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
|[Bad Request: chat not found](json/bad-request-chat-not-found.json )|The chat is unknown to the bot.| Double check the provided `chat_id`|any|
|[Bad request: user not found](json/bad-request-user-not-found.json)|User_id is incorrect|Correct user_id|any|
|[Forbidden: user is deactivated](json/forbidden-user-is-deactivated.json)|You're trying to perform an action on a user account that has been deactivated or deleted| Double check the user I|sendMessage|
|[Forbidden: bot was kicked](json/forbidden-bot-was-kicked.json)|Bot was kicked|Delete `chat_id` on your side|sendMessage|
|[Forbidden: bot blocked by user](json/forbidden-bot-blocked-by-user.json)| The user have blocked the bot ||any|
|[Forbidden: bot can't send messages to bots](json/forbidden-bot-cant-send-messages-to-bots.json)|You tried to send a message to another bot. This is not possible||sendMessage|
|[Too many requests](json/too-many-requests.json)|You are hitting the API limit, [more information here](https://core.telegram.org/bots/faq#my-bot-is-hitting-limits-how-do-i-avoid-this)||sendMessage|
|[Bad request: Group migrated to supergroup](json/bad-request-group-chat-migrated.json)| Occurs when a group chat has been converted/migrated to a supergroup| Check the provided `chat_id` and make sure the new Super Group ID is passed |sendMessage|
|[Bad request: Invalid file id](json/bad-request-invalid-file-id.json)| The file id you are trying to retrieve doesn't exist|Try to call getFile before downloading|getFile|
|[Bad request: Message not modified](json/bad-request-message-not-modified.json)|The current and new message text and reply markups are the same| Actually chanange the text or reply markup of the message to be edited|editMessageText|
|[Conflict: Terminated by other long poll](json/conflicted-terminated-by-other-long-poll.json)|You have already set up a webhook and are trying to get the updates via getUpdates|Do not use getUpdates|getUpdates|
|[Bad request: Wrong parameter action in request](json/bad-request-wrong-parameter-action-in-request.json)| Occurs when the `action` property value is invalid | Provide a valid value to the `action` property as [specified in the documentation](https://core.telegram.org/bots/api#sendchataction) |sendChatAction|
| [Bad Request: message text is empty](json/bad-request-message-text-is-empty.json) | The message text is empty or not provided | Provide a valid message text | sendMessage, editMessageText |
