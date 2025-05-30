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
|[Bad Request: BUTTON_URL_INVALID](json/bad-request-button-url-invalid.json)|Invalid URL format in inline keyboard button|Correct the URL format or protocol|sendMessage, editMessageText|
|[Bad Request: chat not found](json/bad-request-chat-not-found.json )|The chat is unknown to the bot.| Double check the provided `chat_id`|any|
| [Bad Request: message can't be edited](json/bad-request-message-cant-be-edited.json) | The message text cannot be edited | Check is message belong to chat or is message exist in chat | editMessageText |
| [Bad Request: message text is empty](json/bad-request-message-text-is-empty.json) | The message text is empty or not provided | Provide a valid message text | sendMessage, editMessageText |
|[Bad Request: message to delete not found](json/bad-request-message-to-delete-not-found.json)|Message with specified ID doesn't exist|Verify message ID exists in chat|deleteMessage|
|[Bad Request: Group migrated to supergroup](json/bad-request-group-chat-migrated.json)| Occurs when a group chat has been converted/migrated to a supergroup| Check the provided `chat_id` and make sure the new Super Group ID is passed |sendMessage|
|[Bad Request: Invalid file id](json/bad-request-invalid-file-id.json)| The file id you are trying to retrieve doesn't exist|Try to call getFile before downloading|getFile|
|[Bad Request: Message not modified](json/bad-request-message-not-modified.json)|The current and new message text and reply markups are the same| Actually chanange the text or reply markup of the message to be edited|editMessageText|
|[Bad Request: user not found](json/bad-request-user-not-found.json)|User_id is incorrect|Correct user_id|any|
|[Bad Request: Wrong parameter action in request](json/bad-request-wrong-parameter-action-in-request.json)| Occurs when the `action` property value is invalid | Provide a valid value to the `action` property as [specified in the documentation](https://core.telegram.org/bots/api#sendchataction) |sendChatAction|
| [Conflict: can't use getUpdates method while webhook is active; use deleteWebhook to delete the webhook first](json/webhook-is-active.json) | You are trying to use getUpdates while a webhook is active | Use deleteWebhook to delete the webhook first | getUpdates |
|[Conflict: Terminated by other long poll](json/conflicted-terminated-by-other-long-poll.json)|You have already set up a webhook and are trying to get the updates via getUpdates|Do not use getUpdates|getUpdates|
|[Forbidden: bot blocked by user](json/forbidden-bot-blocked-by-user.json)| The user have blocked the bot ||any|
|[Forbidden: bot can't send messages to bots](json/forbidden-bot-cant-send-messages-to-bots.json)|You tried to send a message to another bot. This is not possible||sendMessage|
|[Forbidden: bot was kicked](json/forbidden-bot-was-kicked.json)|Bot was kicked|Delete `chat_id` on your side|sendMessage|
|[Forbidden: user is deactivated](json/forbidden-user-is-deactivated.json)|You're trying to perform an action on a user account that has been deactivated or deleted| Double check the user I|sendMessage|
|[Too many requests](json/too-many-requests.json)|You are hitting the API limit, [more information here](https://core.telegram.org/bots/faq#my-bot-is-hitting-limits-how-do-i-avoid-this)||sendMessage|
|[Unauthorized](json/unauthorized.json)|Bot token is incorrect|Correct your bot token and try again|any|