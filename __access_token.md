# Access token

FoxTrip access token was inspired by JWT system. It uses similar format of data but different construction.

Access token example:
````
4eC39HqLyjWDarjtT1zdp7dc.TMghyEkdC5gmEQRfo26fDvh8qvu1gWHOnAte8g6hmCNwX8U+ZomkTfrcxWZjOmolGIH2FfTxLNKK3C1h/zQ59KMKExPwlfLYLAEzLyE5bQIhx/589CLRsAM+ufNAD/GK6uiT06qiUNx2nxDb3YYko0tO3KgFUrQ==
````

The access token consists of two parts: `API key` and `payload` which are sipareted by symbol `.` (dot). 

`API key` is unique generated key by API server after registration in the system and encripted by Base64. `API key` is always 50 bytes.

`Payload` is JSON document with user data and request which is encripted by `session key`. Length of this field always depends on length of `email` and `passwords`.

`Payload` contains next fields:
````json
{
    "email": "alisa.holms@eugeneslab.net",
    "password": "pmWkWSBCL51Bfkhn79xPuKBKHz//H6B+mY6G9/eieuM=",
    "md5": "h5ub/JvXjdD6B8bZqzeaMQ=="
}
````
- `email` - email of user which he/she used in registration
- `password` - hash of a password of the user which he/she used in registration
- `md5` - hash sum of a body of a request which was obtained MD5 hashing. This field will guarantee that the data which the user sent in request will not be changed on the way by somebody else or as a result of collissions.  

The server will compare `email` and `password` with data from database. If `email` or `password` will not match with those data which user specified during registration the server will return error **401 Unauthorized**. The same is with `md5`: if hash sum will not equel to hash sum of the body of the request, the server will return **400 Bad Request**.
