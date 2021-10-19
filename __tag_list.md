# Getting tags (40)
Any host may send request to get list of tags

````
GET /api/v1/request?t=40 HTTP/1.1
Content-Language: CZ-cz
````

### Response

```` json
{
    "tags" :
    [
        {
            "id"    : "1",
            "title" : "Forest"
        },

        {
            "id"    : "2",
            "title" : "Castle"
        }
    ]
}
````