# Deleting users (18)

A host with privileges may delete other users in the system. Hosts who has role **Member** cannot delete users who have role **Admin**. There are also restrictions according permissions list such as **[mightDeleteUsers](/__user_permissions?id=mightDeleteUsers)** .

````
DELETE /api/v1/requests?t=18&id=$userId$ HTTP/1.1
Access-Token: 4eC39HqLyjWDarjtT1zdp7dc
````

### Arguments
**id** - requierd field. Defines user ID who has to be deleted from the system

### Response
If the request was accepted succesfully, the server will return response **200 OK**. Another way it may return one of the error statuses