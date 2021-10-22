# Creating route (30)
Users who have privileges can send this request to create a new route. To send request the host must have API key and role appropriate admin or memeber.

````
POST /api/v1/request?t=30 HTTP/1.1
Access-Token: 4eC39HqLyjWDarjtT1zdp7dc
````

### Response
````json
{
    "id": "1"
}
````