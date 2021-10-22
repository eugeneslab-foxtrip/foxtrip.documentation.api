# Getting news list (21)

Any user may requests news. The HTTP request has to contain header *Content-Language* which defines languege of content which reqiers. If there is no selected languege then the server will return the **404 Not Found** status

````
GET /api/v1/request?t=21&page=1&limit=20&public=0 HTTP/1.1
Content-Language: CZ-cz
````
### Arguments
**page** - requier argument. This defines number of page

**limit** - requier argument. This defines limiting results for one page

**public** - this flag defines if to show only publicated news. *1* - only publicated and *0* - only not publicated news. If this argument is not defined then it returns publicated and not publicated news together

### Response

```` json
{
    "number": "158",

    "page": 
    [
        {
            "id"            : "1",
            "cover"         : "/album/lorem.png",
            "datetime"      : "155748321874",
            "title"         : "Lorem Ipsum is simply dummy text of the printing",
            "content"       : "Lorem Ipsum has been the industry's standard dummy text",
            "publicated"    : "false"
        },
        
        {
            "id"            : "2",
            "cover"         : "http://127.0.0.1/album/contrary.png",
            "datetime"      : "1557483218465",
            "title"         : "Contrary to popular belief, Lorem Ipsum...",
            "content"       : "Lorem Ipsum has been the industry's standard dummy text",
            "publicated"    : "true"
        }
    ]
}
````

The field *number* defines how many items database contains.