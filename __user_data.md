# Getting account

This command provides **GET** request and as answer you are able to get full data about user. The user must be authorizated before sending this request, another way response will be as the code **401 Unauthorized**

````
GET /api/v1/user/$userId$ HTTP/1.1
````
### Arguments
**userId** - User ID from database which data the host requests

### Response

If request was succesfull the response will contain body with data in JSON format. For example:

```` json
{
    "id"            : "1",
    "role_id"       : "1",
    "email"         : "example@email.com",
    "name"          : "Tomas",
    "surname"       : "Tailor",
    "ban"           : "false",
    "api-key"       : "4eC39HqLyjWDarjtT1zdp7dc",
}
````

Another way a server may return next statuses:

* **400 Bad request** 
* **401 Unauthorized**
* **403 Forbidden**