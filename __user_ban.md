# Banning a user

A host with privileges may ban any user in the system. The request provides **PUT** method. To send this request it is necassary to have API key and permission **[mightBan](/__user_permissions?id=mightBan)**.

````
PUT /api/v1/user-ban/$userId$ HTTP/1.1
````
### Arguments

**userId** - User ID from database which data the host requests

### Response

If the request was accepted succesfully, the server will return response **200 OK**. Another way it may return:

* **400 Bad request** 
* **401 Unauthorized**
* **403 Forbidden**