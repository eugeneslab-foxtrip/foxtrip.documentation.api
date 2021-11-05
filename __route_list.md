# Gettings routes (31)
Any user may requests routes. The HTTP request has to contain header *Content-Language* which defines languege (BCP47) of content which reqiers. If there is no selected languege then the server will return the **404 Not Found** status.

If the request contains *Access-Token* header and the user doesn't have role lower then **Member**, the server will return publicated and unpublicated routes
```
GET /api/v1/request?t=31&page=1&limit=20&public=1 HTTP/1.1
Access-Token: 4eC39HqLyjWDarjtT1zdp7dc
Content-Language: cs-CZ
```

### Arguments
**page** - requier argument. This defines number of page

**limit** - requier argument. This defines limiting results for one page

**public** - this flag defines if to show only publicated routes. *1* - only publicated and *0* - only not publicated routes. If this argument is not defined then it returns publicated and not publicated routes together if *Access-Token* is defined, another way it returns only publicated routes

### Searching filtr
**title** - defines searching filtr by title or some phrases from title

**dist-from** - defines searching filtr by distance range in metres. If the argument was't defined the server will not consider lower limit

**dist-to** - defines searching filtr by distance range in metres. If the argument was't defined the server will not consider upper limit

**tags** - defines searching filtr by tags. This arguments contains list of tags devided by symbol ",", for example:
````
GET /api/v1/request?t=31&page=1&limit=20&tags=1,2,3 HTTP/1.1
````

### Response
````json
{
    "page": 
    [
        {
            "id"            : "1",
            "cover"         : "http://127.0.0.1/album/lorem.png",
            "title"         : "Lorem Ipsum is simply dummy text of the printing",
            "distance"      : "2650",
            "publicated"    : "true"
        },
        
        {
            "id"            : "2",
            "cover"         : "http://127.0.0.1/album/contrary.png",
            "distance"      : "1250",
            "title"         : "Contrary to popular belief, Lorem Ipsum...",
            "publicated"    : "true"
        }
    ]
}
````