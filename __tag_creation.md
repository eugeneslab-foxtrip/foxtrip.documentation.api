# Create tag (40)
Users who have privileges can send this request to create a tag. To send request the host must have API key and role appropriate *admin* or *memeber*. The HTTP request has to contain header *Content-Language* which defines languege of content which reqiers
````
POST /api/v1/request?t=40 HTTP/1.1
Content-Language: CZ-cz
Access-Token: 4eC39HqLyjWDarjtT1zdp7dc
````
```` json
{
    "title": "Lorem"
}
````

### Response
```` json
{
    "id": "1"
}
````