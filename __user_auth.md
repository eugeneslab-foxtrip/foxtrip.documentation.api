# Authorization (2)

Registerted users may be authorized in the system to extend order of requests.

````
POST /api/v1/request?t=2 HTTP/1.1
````
```` json
{
    "id" : "3",
    "password" : "mpxBYOaI/rOmgyk/0Z6eT3mqSrToHibo9Amxsnaun+E="
}
````

The user has to send his real password which has to be encripted by sesssion key. The server will check if hash of your passowrd mathes with hash from database. If authorization was saccessful the server will return **200 OK**. Another way it will return one of the error statuses. 