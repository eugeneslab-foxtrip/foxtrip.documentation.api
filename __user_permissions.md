# Permissions (13)
The server may allow or deny of some type of requests according the permissions list. Privileges users are able to edit permissions for other users of the system. Permissions represent list of *bool* variables which allow or deny specific operations. 
````
PUT /api/v1/request?t=13&id=3 HTTP/1.1
Access-Token: 4eC39HqLyjWDarjtT1zdp7dc
````
```` json
{
    "mightBan"             :   "true",
    "mightPublicateNews"   :   "false"
}
````

### Arguments
**id** - requierd field. Defines user ID who permissions has to be updated

A host who is going to update permissions has to send in body only those variables which requier to be updated 

### Response
If the request was accepted succesfully, the server will return response **200 OK**. Another way it may return one of the error statuses

### Permissions list
#### mightUpdatePermissions
Defines possobility of selected user change permissions of other users

#### mightBan
Defines possobility of selected user to block other users

#### mightDeleteUsers
Defines possobility of selected user to delete other users

#### mightPublicateNews
Defines possobility of selected user publucate news and aticles after creating and editing

#### mightEditNews
Defines possobility of selected user edit news and aticles after creating

#### mightCreateNews
Defines possobility of selected user to create news and aticles
