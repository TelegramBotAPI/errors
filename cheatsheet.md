| JSON         | Human Description| Action needed?    | Methods raising |
|--------------|------------------|-------------------|-----------------|
|`{"ok":false,"error_code":401,"description":"Unauthorized"}`|Bot token is incorrect|Correct your bot token and try again|any|
|`{"ok":false,"error_code":400,"description":"Bad Request: chat not found"}`|||any|
|`{"ok":false,"error_code":400,"description":"[Error]: Bad Request: user not found"}`|User_id is incorrect|Correct user_id|any|
|`{"ok":false,"error_code":403,"description":"Forbidden: user is deactivated"} `|||sendMessage<br />any(?)|
|`{"ok":false,"error_code":403,"description":"Forbidden: bot was kicked from the group chat"}`|Bot was kicked|Delete chat_id on your side|sendMessage|
|`{"ok":false,"error_code":403,"description":"Forbidden: bot was blocked by the user"}`|||any|
|`{"ok":false,"error_code":429,"description":"Too Many Requests: retry after X","parameters":{"retry_after":X}}`|You are hitting the API limit, more information here||sendMessage|
|`{"ok":false,"error_code":400,"description":"Bad Request: group chat was migrated to a supergroup chat","parameters":{"mi (truncated...)`||sendMessage|
|`{"ok":false,"error_code":400,"description":"Bad Request: invalid file id"}`| The file id you are trying to retrieve doesn't exist|Try to call getFile before downloading|getFile|
|`{"ok":false,"error_code":400,"description":"Bad Request: message is not modified"}`|||EditMessage*|
