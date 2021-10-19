# Update publication (31)
Users who have privileges can send this request to update publication. To send request the host must have API key and role appropriate *admin* or *memeber*. The HTTP request has to contain header *Content-Language* which defines languege of content which reqiers
````
PUT /api/v1/request?t=31&id=1 HTTP/1.1
Content-Language: CZ-cz
Access-Token: 4eC39HqLyjWDarjtT1zdp7dc
````
```` json
{
    "cover"         : "http://127.0.0.1/picture/lorem.png",
    "title"         : "Lorem ipsum dolor sit amet, consectetur adipiscing elit",
    "content"       : "sed do eiusmod tempor incididunt ut labore et dolore",
    "publicated"    : "false"
}
````
### Arguments
**id** - reqiered argument. This defines indentificator of a publication

### Response
The server will return **200 Ok** status if the request has been processed