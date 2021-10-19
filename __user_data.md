# Getting account (11)

This command provides **GET** request and as answer you are able to get full data about user. The user must be authorizated before sending this request, another way response will be as the code **401 Unauthorized**

````
GET /api/v1/request?t=11&id=$userId$ HTTP/1.1
Access-Token: 4eC39HqLyjWDarjtT1zdp7dc
````
### Arguments
**id** - requierd field. Defines user ID from database. If the server will not able to find the user with current Id, response will return **404 Not Found** 

### Response

If request was succesfull the response will contain encripted data. Behind encripted data is user data in JSON format. For example:

```` json
{
    "id"            : "1",
    "role_id"       : "1",
    "email"         : "example@email.com",
    "name"          : "Tomas",
    "surname"       : "Tailor",
    "ban"           : "false"
}
````

Another way a server may return one of the error statuses