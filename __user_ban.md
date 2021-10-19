# Banning a user (12)

A host with privileges may ban any user in the system. The request provides **PUT** method. To send this request it is necassary to have API key and permission **[mightBan](/__user_permissions?id=mightBan)**.

````
PUT /api/v1/request?t=12&id=$userId$ HTTP/1.1
Access-Token: 4eC39HqLyjWDarjtT1zdp7dc
````
### Arguments

**id** - requierd field. Defines user ID from database. If the server will not able to find the user with current Id, response will return **404 Not Found** 

### Response

If the request was accepted succesfully, the server will return response **200 OK**. Another way it may return one of the error statuses