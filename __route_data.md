# Getting route (30)

````
GET /api/v1/request?t=30&id=1 HTTP/1.1
````

### Arguments
**id** - reqiered argument. This defines indentificator of a route which was requested

### Response
````json
{
    "id": "1",
    "cover": "http://127.0.0.1/album/lorem.png",
    "title": "Lorem Ipsum is simply dummy text of the printing",
    "description": "Lorem Ipsum has been the industry's standard dummy text",
    "distance": "2650",
    "publicated": "false",

    "tags": 
    [
        {
            "id": "1"
        }
    ],

    "places":
    [
        {
            "id": "1",
            "title": "Lorem ipsum",
            "tag": "2"
        }
    ],

    "album":
    [
        {
            "picture": "http://127.0.0.1/album/1.png"
        }    
    ],

    "track":
    [
        {
            "id": "1",
            "title": "Lorem Ipsum",
            "description": "industry's standard dummy",
            "lon": "16.52529090642929",
            "lat": "49.22410972416401",
            "direction": "1",
            "distance": "380",
            "sings":
            [
                {
                    "id": "1"
                }
            ]
        }
    ]
}
````