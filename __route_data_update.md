# Update route (30)

````
PUT /api/v1/request?t=30&id=1 HTTP/1.1
Content-Language: CZ-cz
Access-Token: 4eC39HqLyjWDarjtT1zdp7dc
````
````json
{
    "cover": "http://127.0.0.1/album/lorem.png",
    "title": "Lorem Ipsum is simply dummy text of the printing",
    "description": "Lorem Ipsum has been the industry's standard dummy text",
    "distance": "2650",

    "tags": 
    [
        {
            "id": "1"
        }
    ]
}
````

### Publication route
````
PUT /api/v1/request?t=30&id=1 HTTP/1.1
Access-Token: 4eC39HqLyjWDarjtT1zdp7dc
````
````json
{
    "publicated": "true"
}
````


### Response
The server will return **200 Ok** status if the request has been processed