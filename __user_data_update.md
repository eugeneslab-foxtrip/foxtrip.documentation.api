# Update account (18)

Any host who has access to the system may update their own account data. Privileges hosts might update accounts data of users who has lower privilege, for example **admin** has possobility to change data of any users in the system, but **memer** cannot change data of admin, but may change users who have **guest** role. If host will try to change account data who doesn't have permission to do that, host will get response **403 Forbidden**. A host also must be authorizated in the system, another way the host will get response **401 Unauthorized**.

````
PUT /api/v1/request?t=19 HTTP/1.1
Access-Token: 4eC39HqLyjWDarjtT1zdp7dc
````
```` json
{
    "id"    : "1",
    "email" : "alisa@email.com"
}
````

The body of request has to contain ***id*** of user for updating and fields which requierd to rewrite. Success response is **200 OK**, another way the server may return one of the error statuses