# Deleting route (30)
Users who have privileges can send this request to delete a route. To send request the host must have API key and role appropriate `admin` or `memeber`. This request will also  delete all existed translations 
````
DELETE /api/v1/request?t=30 HTTP/1.1
Access-Token: 4eC39HqLyjWDarjtT1zdp7dc
````
````json
{
    "id": "1"
}
````
### Arguments
**id** - reqiered argument. This defines indentificator of the route

### Response
If the request has been procced successful the server will return the status **200 Ok**