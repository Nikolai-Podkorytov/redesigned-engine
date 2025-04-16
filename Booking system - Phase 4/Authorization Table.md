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













