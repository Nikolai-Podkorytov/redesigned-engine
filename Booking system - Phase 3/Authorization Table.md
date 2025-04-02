**Authorization Table**

| **Page / Feature** | **Guest** | **Reserver** | **Administrator** |
|:----|:----:|:----:|:----:|
| `/` (index)                | ✅ | ✅ | ✅ |
| └─ Create new resource     | ⚠️ *2  | ✅ | ✅ |
| └─ View resource form      | ❌ | ✅ | ✅  |
| └─ V Booked resources | ✅ | ✅ | ✅ |
| └─ V emails of users with reservations | ❌ | ✅ | ✅ |
| `/reservation` | ❌ | ✅ | ✅ |
| └─ Creating a reservation | ❌ | ✅ *1 | ✅ |
| `/resources`| ⚠️ *2 |  ✅ |  ✅ |
| └─ Creating a reservation |  ⚠️ *2 | ✅  | ✅  |
| └─ View Add a new reservation form      | ❌ | ✅ | ✅  |
| `/login` | ✅   |  ⚠️ *2 |  ⚠️ *2 |
| └─ Login as "reserver" user |  ✅ |  ⚠️ *2 | ⚠️ *2  |
| └─ Login as "administrator" user | ✅  |  ⚠️ *2 | ⚠️ *2 |
| `/register` | ✅  | ⚠️ *2 | ⚠️ *2 |
| └─ Create a user with "reserver" role | ✅ | ⚠️ *2 | ⚠️ *2 |
| └─ Create a user with "administrator" role | ✅ | ⚠️ *2 | ⚠️ *2 |
| `/logout` | ❌  |  ✅ | ✅  |
| `/api/users` | ⚠️ *2 | ⚠️ *2 | ⚠️ *2 |
| `/api/resources` |  ⚠️ *2|  ⚠️ *2| ⚠️ *2 |
| `/api/session` | ⚠️ *2 | ⚠️ *2 |⚠️ *2  |
| `/resources?id=`  | ❌ | ✅ | ✅ |
| └─ Edit own resource | ❌ | ✅ | ✅|
| └─ Edit other's resource | ❌ | ⚠️ *2 | ✅ |
| `/reservation?id=` | ❌ | ✅ | ✅ |
| └─ Edit own reservation | ❌ | ✅ | ✅|
| └─ Edit others' reservations | ❌ | ⚠️ *2 | ✅ |

**Notes for Authorization Table:**  
1. Only if the user's date of birth is 15 years or older.
2. through address bar


**Symbols used:**  
✅ Pass   
❌ Fail   
⚠️ Attention 










**Notes:**
```
REserver 

Test@doe.com 
123456789


admin@gmail.com
987654321














000000001:   200        27 L     121 W      1921 Ch     "http://localhost:8000/"                                                                                                        
000002362:   302        0 L      0 W        0 Ch        "logout"                                                                                                                        
000002347:   200        32 L     137 W      1967 Ch     "login"                                                                                                                         
000003341:   200        44 L     202 W      2978 Ch     "register"                                                                                                                      
000003404:   200        38 L     157 W      2235 Ch     "resources"                                                                                                                     
000003395:   401        0 L      1 W        12 Ch       "reservation"  



********************************************************
* Wfuzz 3.1.0 - The Web Fuzzer                         *
********************************************************

Target: http://localhost:8000/api/FUZZ
Total requests: 4614

=====================================================================
ID           Response   Lines    Word       Chars       Payload                                                                                                                         
=====================================================================

000003404:   200        0 L      1 W        2 Ch        "resources"                                                                                                                     
000003601:   401        0 L      1 W        12 Ch       "session"                                                                                                                       
000004245:   200        0 L      1 W        99 Ch       "users"                                                                                                                         

Total time: 0
Processed Requests: 4614
Filtered Requests: 4611
Requests/sec.: 0




└─$ wfuzz -c -z range,1-1000 --hc 404 http://localhost:8000/api/reservations/FUZZ
********************************************************
* Wfuzz 3.1.0 - The Web Fuzzer                         *
********************************************************

Target: http://localhost:8000/api/reservations/FUZZ
Total requests: 1000

=====================================================================
ID           Response   Lines    Word       Chars       Payload                                                                                                                         
=====================================================================

000000001:   200        0 L      1 W        184 Ch      "1"                                                                                                                             
000000002:   200        0 L      1 W        184 Ch      "2"                                                                                                                             

Total time: 1.158113
Processed Requests: 1000
Filtered Requests: 998
Requests/sec.: 863.4728




┌──
└─$ http http://localhost:8000/api/reservations/1  
HTTP/1.1 200 OK
content-encoding: gzip
content-length: 153
content-security-policy: default-src 'self'; script-src 'self'; style-src 'self'; img-src 'self'; frame-ancestors 'none'; form-action 'self';
content-type: application/json
date: Tue, 01 Apr 2025 11:34:35 GMT
vary: Accept-Encoding
x-content-type-options: nosniff
x-frame-options: DENY

{
    "reservation_end": "2025-04-10T00:00:00.000Z",
    "reservation_id": 1,
    "reservation_start": "2025-04-01T16:05:00.000Z",
    "reserver_token": "95268b1b-4efb-4981-acfb-47e16dbec106",
    "resource_id": 2
}

```

