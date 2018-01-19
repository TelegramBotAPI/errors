| JSON         | Human Description| Action needed?    |
|--------------|------------------|-------------------|
|`{"ok":false,"error_code":400,"description":"Bad Request: invalid file id"}`| The file id you are trying to retrieve doesn't exist|Try to call getFile before downloading|
|`{"ok":false,"error_code":401,"description":"Unauthorized"}`|Bot token is incorrect|Correct your bot token and try again|
|`{"ok":false,"error_code":400,"description":"[Error]: Bad Request: user not found"}`|User_id is incorrect|Correct user_id|
|`{"ok":false,"error_code":403,"description":"Forbidden: bot was kicked from the group chat"}`|Bot was kicked|Delete chat_id on your side|
|`{"ok":false,"error_code":400,"description":"Bad Request: chat not found"}`|?|?|
