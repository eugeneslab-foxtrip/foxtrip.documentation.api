# Banning a user (16)

A host with privileges may ban any user in the system. The request provides **PUT** method. To send this request it is necassary to have API key and permission **[mightBan](/__user_permissions?id=mightBan)**.

````
PUT /api/v1?request=16&id=$userId$ HTTP/1.1
````
### Arguments

**id** - user ID from database

### Response

If the request was accepted succesfully, the server will return response **200 OK**. Another way it may return:

* **400 Bad request** 
* **401 Unauthorized**
* **403 Forbidden**