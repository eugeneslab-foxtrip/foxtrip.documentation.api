# Creating route (30)
Users who have privileges can send this request to create a new route. To send request the host must have API key and role appropriate `admin` or `memeber`.

The HTTP request has to contain header *Content-Language* which defines languege (BCP47) of content which reqiers. If there is no selected languege then the server will return the **400 Bad Request** status.
````
POST /api/v1/request?t=30 HTTP/1.1
Access-Token: 4eC39HqLyjWDarjtT1zdp7dc
Content-Language: cs-CZ
````
````json
{
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
            "id": "1"
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
!> Not all objects of the JSON body request is requierd except for `title` field. If a field wasn't defined the server will leave this data withot changes.


### Response
````json
{
    "id": "1"
}
````