# Getting list of users (19)

Users who have privileges can send request list of registered users. To send request the host must have API key and role appropriate **admin** or **memeber**. 

````
GET /api/v1?request=19&page=$pageNumber$ HTTP/1.1
````
### Arguments
**page** - page number for request users. Every page contains 20 users. If a host requests page number more then exist, array block will be empty in response body.


### Response

If request was succesfull the response will contain body with data in JSON format. For example:

```` json
{
    "pageNumber"        : "1",
    "pageCount"         : "3"

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

Another way it may return:

* **400 Bad request** 
* **401 Unauthorized**
* **403 Forbidden**