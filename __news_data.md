# Getting news (20)

Any user may requests publications. The HTTP request has to contain header *Content-Language* which defines languege of content which reqiers. If there is no selected languege then the server will return the **404 Not Found** status

````
GET /api/v1/request?t=20&id=1 HTTP/1.1
Content-Language: CZ-cz
````
### Arguments
**id** - reqiered argument. This defines indentificator of publication which was requested

### Response

```` json
{
    "id"        : "1",
    "cover"     : "http://127.0.0.1/album/lorem.png",
    "datetime"  : "155748321874",
    "title"     : "Lorem Ipsum is simply dummy text of the printing",
    "content"   : "Lorem Ipsum has been the industry's standard dummy text"
}
````