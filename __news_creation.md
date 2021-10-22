# Creating publication (20)
Users who have privileges can send this request to create publication. To send request the host must have API key and role appropriate *admin* or *memeber*. The HTTP request has to contain header *Content-Language* which defines languege of content which reqiers
````
POST /api/v1/request?t=20 HTTP/1.1
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
### Response
The server will return indentificator of created publication if the request was successful. Another way the server will return a status error 
```` json
{
    "id" : "1"
}
````