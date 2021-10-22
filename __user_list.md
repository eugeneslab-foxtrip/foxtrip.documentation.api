# Getting list of users (10)

Users who have privileges can send request list of registered users. To send request the host must have API key and role appropriate **admin** or **memeber**. 

````
GET /api/v1/request?t=10&page=1&limit=20 HTTP/1.1
Access-Token: 4eC39HqLyjWDarjtT1zdp7dc
````
### Arguments
**page** - requierd field. Defines page number for request users. Every page contains 20 users. If a host requests page number more then exist, response will return **404 Not Found**

**limit** - requierd field. Defines count of users which one page might contain

### Searching filtr

**email** - defines searching filtr by email or a part of email

**role** - defines searching filtr by role

### Response

If request was succesfull the response will contain encripted data. Behind encripted data is user data in JSON format. For example:

```` json
{
    "number": "15",
    "page": 
    [
        {
            "id"        : "1",
            "role_id"   : "1",
            "email"     : "bob@email.com",
            "name"      : "Bob",
            "surname"   : "Mask",
            "ban"       : "false"
        },
        
        {
            "id"        : "2",
            "role_id"   : "3",
            "email"     : "alisa@email.com",
            "name"      : "Alisa",
            "surname"   : "Holms",
            "ban"       : "false"
        }
    ]
}
````

Another way it may return: one of the error statuses. The field *number* defines how many items database contains.