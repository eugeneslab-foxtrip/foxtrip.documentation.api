# Getting statistic

Any hosts can request the statistic withoute any restriction. Statistic contains next points:
- Number of users who has "Admin" role
- Number of users who has "Member" role
- Number of users who has "Guest" role
- Number of news (common number of all news in the system)
- Number publicated news
- Number of routes (common number of all routes in the system)
- Number of publicated routes
- Number of cities
- Number of tags
- Number of pictures

````
GET /api/v1/request?t=20
````

### Response

When the request was processed successful, the host will get response with code **200 OK** and JSON data in body, for example:

```` json
{
    "admin_users"       : "1",
    "member_users"      : "2",
    "guest_users"       : "27",
    "news"              : "10",
    "publicated_news"   : "4",
    "routes"            : "10",
    "publicated_routes" : "3",
    "cities"            : "112",
    "tags"              : "6",
    "pictures"          : "12"
}
````

When the request was failed the server will return response **400 Bad Request**