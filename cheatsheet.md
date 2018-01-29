| JSON         | Human Description| Action needed?    | Methods raising |
|--------------|------------------|-------------------|-----------------|
|[Unauthorized](json/unauthorized.json)|Bot token is incorrect|Correct your bot token and try again|any|
|[Bad Request: chat not found](json/bad-request-chat-not-found.json )|||any|
|[Bad request: user not found](json/bad-request-user-not-found.json)|User_id is incorrect|Correct user_id|any|
|[Forbidden: user is deactivated](json/forbidden-user-is-deactivated.json)|||SendMessage<br />any(?)|
|[Forbidden: bot was kicked](json/forbidden-bot-was-kicked.json)|Bot was kicked|Delete chat_id on your side|SendMessage|
|[Forbidden: bot blocked by user](json/forbidden-bot-blocked-by-user.json)|||any|
|[Too many requests](json/too-many-requests.json)|You are hitting the API limit, more information here||SendMessage|
|[Bad request: Group migrated to supergroup](json/bad-request-group-chat-migrated.json)||SendMessage|
|[Bad request: Invalid file id](json/bad-request-invalid-file-id.json)| The file id you are trying to retrieve doesn't exist|Try to call getFile before downloading|GetFile|
|[Bad request: Message not modified](json/bad-request-message-not-modified.json)|||EditMessageText|
