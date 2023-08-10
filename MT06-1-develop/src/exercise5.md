### 1. GET ​/api​/v1​/Activities
HTTP-метод: GET     
Полный URL запрос: <https://fakerestapi.azurewebsites.net/api/v1/Activities>  
Заголовки запроса:  "accept: text/plain; v=1.0"    
Тело запроса (при наличии): отсутсвует  
Статус-код ответа: 200   
Тело ответа (при наличии):   
```
[   
  {
    "id": 1,
    "title": "Activity 1",
    "dueDate": "2023-05-30T10:36:43.756403+00:00",
    "completed": false
  },
  {
    "id": 2,
    "title": "Activity 2",
    "dueDate": "2023-05-30T11:36:43.7564053+00:00",
    "completed": true
  },
  {
    "id": 3,
    "title": "Activity 3",
    "dueDate": "2023-05-30T12:36:43.7564055+00:00",
    "completed": false
  },
  {
    "id": 4,
    "title": "Activity 4",
    "dueDate": "2023-05-30T13:36:43.7564058+00:00",
    "completed": true
  },
  {
    "id": 5,
    "title": "Activity 5",
    "dueDate": "2023-05-30T14:36:43.7564061+00:00",
    "completed": false
  },
  {
    "id": 6,
    "title": "Activity 6",
    "dueDate": "2023-05-30T15:36:43.7564067+00:00",
    "completed": true
  }
]
```

### 2. POST ​/api​/v1​/Activities  Удачный
HTTP-метод: POST     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Activities   
Заголовки запроса: "accept: text/plain; v=1.0"      
Тело запроса (при наличии):       
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-05-30T09:57:15.691Z",
  "completed": true
} 
``` 
Статус-код ответа: 200   
Тело ответа (при наличии):   
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-05-30T09:57:15.691Z",
  "completed": true
}
```

### 3. POST ​/api​/v1​/Activities  Провальный
HTTP-метод: POST     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Activities   
Заголовки запроса: "accept: text/plain; v=1.0"      
Тело запроса (при наличии):       
```
{
  "id": 58588888888888585285,
  "title": "string",
  "dueDate": "2023-05-30T16:00:45.762Z",
  "completed": true
}
``` 
Статус-код ответа: 400   
Тело ответа (при наличии):   
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-a45f8e1cb27fb546bb269406f6bb1530-8c0cd9da139dad44-00",
  "errors": {
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 26."
    ]
  }
}
```

### 4. GET ​/api​/v1​/Activities​/{id}  Удачный

HTTP-метод: GET     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Activities/1   
Заголовки запроса: "accept: text/plain; v=1.0"     
Тело запроса (при наличии):       
Статус-код ответа: 200   
Тело ответа (при наличии):   
```
{
  "id": 1,
  "title": "Activity 1",
  "dueDate": "2023-05-30T17:03:52.5036034+00:00",
  "completed": false
}
```

### 5. GET ​/api​/v1​/Activities​/{id}   Провальный
HTTP-метод: GET     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Activities/16554566666666664687    
Заголовки запроса: "accept: text/plain; v=1.0"     
Тело запроса (при наличии):       
Статус-код ответа: 400   
Тело ответа (при наличии):   
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-c722c1fc45ef7e48bbc2dd188d4e6ba1-7d32a17d32c77a48-00",
  "errors": {
    "id": [
      "The value '16554566666666664687' is not valid."
    ]
  }
}
```

### 6. PUT /api​/v1​/Activities​/{id}  Удачный
HTTP-метод: PUT     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Activities/1    
Заголовки запроса: "accept: text/plain; v=1.0"     
Тело запроса (при наличии):       
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-05-30T16:15:38.465Z",
  "completed": true
}
```
Статус-код ответа: 200   
Тело ответа (при наличии):   
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-05-30T16:15:38.465Z",
  "completed": true
}
```

### 7. PUT /api​/v1​/Activities​/{id}  Провальный 
HTTP-метод: PUT     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Activities/1    
Заголовки запроса: "accept: text/plain; v=1.0"     
Тело запроса (при наличии):       
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-05-30T16:15:38.465Z",
  "completed": true
}
```
Статус-код ответа: 400   
Тело ответа (при наличии):   
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-be9bec7ea183a947ba924500db15cdd7-f5ed57d934b76b40-00",
  "errors": {
    "id": [
      "The value '122228777777777777' is not valid."
    ]
  }
}
```

### 8. DELETE ​/api​/v1​/Activities​/{id}  
HTTP-метод: DELETE     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Activities/12   
Заголовки запроса: "accept: */*"     
Тело запроса (при наличии):отсутсвует       
Статус-код ответа: 200   
Тело ответа (при наличии): отсутсвует   

###  9. GET ​/api​/v1​/Authors 
HTTP-метод: GET     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Authors     
Заголовки запроса: "accept: text/plain; v=1.0"     
Тело запроса (при наличии):отсутсвует       
Статус-код ответа: 200   
Тело ответа (при наличии):
```
[
  {
    "id": 1,
    "idBook": 1,
    "firstName": "First Name 1",
    "lastName": "Last Name 1"
  },
  {
    "id": 2,
    "idBook": 1,
    "firstName": "First Name 2",
    "lastName": "Last Name 2"
  },
  {
    "id": 3,
    "idBook": 1,
    "firstName": "First Name 3",
    "lastName": "Last Name 3"
  },
  {
    "id": 4,
    "idBook": 1,
    "firstName": "First Name 4",
    "lastName": "Last Name 4"
  },
  {
    "id": 5,
    "idBook": 2,
    "firstName": "First Name 5",
    "lastName": "Last Name 5"
  },
  {
    "id": 6,
    "idBook": 2,
    "firstName": "First Name 6",
    "lastName": "Last Name 6"
  }
]
```

### 10. POST ​/api​/v1​/Authors  Удачный
HTTP-метод: POST     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Authors     
Заголовки запроса: "accept: text/plain; v=1.0"     
Тело запроса (при наличии):
```
{
  "id": 2,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```     
Статус-код ответа: 200   
Тело ответа (при наличии):
```
{
  "id": 2,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```

### 11. POST ​/api​/v1​/Authors Провальный 
HTTP-метод: POST     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Authors     
Заголовки запроса: "accept: text/plain; v=1.0"     
Тело запроса (при наличии):
```
{
  "id": 355555555544534343,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
Статус-код ответа: 400   
Тело ответа (при наличии):
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-f782d37c1f19894fa6b29f0d56b7f2d2-f1f1eef4ab34b14b-00",
  "errors": {
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 24."
    ]
  }
}
```

### 12. GET ​/api​/v1​/Authors​/authors​/books​/{idBook} Удачный    
HTTP-метод: GET     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/1     
Заголовки запроса: "accept: text/plain; v=1.0"     
Тело запроса (при наличии): отсутствует
Статус-код ответа: 200   
Тело ответа (при наличии):
```
[
  {
    "id": 1,
    "idBook": 1,
    "firstName": "First Name 1",
    "lastName": "Last Name 1"
  },
  {
    "id": 2,
    "idBook": 1,
    "firstName": "First Name 2",
    "lastName": "Last Name 2"
  },
  {
    "id": 3,
    "idBook": 1,
    "firstName": "First Name 3",
    "lastName": "Last Name 3"
  }
]
```

### 13. GET ​/api​/v1​/Authors​/authors​/books​/{idBook} Провальный   
HTTP-метод: GET     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/1565465467567567      
Заголовки запроса: "accept: text/plain; v=1.0"     
Тело запроса (при наличии): отсутствует
Статус-код ответа: 400   
Тело ответа (при наличии):
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-846befc18147734d8f5f6d80a595e62b-f13e4a8c84d7554a-00",
  "errors": {
    "idBook": [
      "The value '1565465467567567' is not valid."
    ]
  }
}
```

### 14. GET ​/api​/v1​/Authors​/{id} Удачный     
HTTP-метод: GET     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Authors/1      
Заголовки запроса: "accept: text/plain; v=1.0"     
Тело запроса (при наличии): отсутствует
Статус-код ответа: 200   
Тело ответа (при наличии):
```
{
  "id": 1,
  "idBook": 1,
  "firstName": "First Name 1",
  "lastName": "Last Name 1"
}
```

### 15. GET ​/api​/v1​/Authors​/{id} Провальный     
HTTP-метод: GET     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Authors/14353463464       
Заголовки запроса: "accept: text/plain; v=1.0"     
Тело запроса (при наличии): отсутствует
Статус-код ответа: 400   
Тело ответа (при наличии):
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-5074e2bf514d6d49abe7760276dd4090-a922d9f8bc49cf4a-00",
  "errors": {
    "id": [
      "The value '14353463464' is not valid."
    ]
  }
}
```

### 16. PUT ​/api​/v1​/Authors​/{id} Удачный      
HTTP-метод: PUT     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Authors/1       
Заголовки запроса: "accept: text/plain; v=1.0"     
Тело запроса (при наличии): 
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
Статус-код ответа: 200   
Тело ответа (при наличии):
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```

### 17. PUT ​/api​/v1​/Authors​/{id} Провальный      
HTTP-метод: PUT     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Authors/525252525525       
Заголовки запроса: "accept: text/plain; v=1.0"     
Тело запроса (при наличии): 
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
Статус-код ответа: 400   
Тело ответа (при наличии):
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-aa0b13590c799d4489b379c6af72f40b-77c212649332884f-00",
  "errors": {
    "id": [
      "The value '525252525525' is not valid."
    ]
  }
}
```

### 18. DELETE ​/api​/v1​/Authors​/{id} 
HTTP-метод: DELETE     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Authors/1   
Заголовки запроса: "accept: */*"     
Тело запроса (при наличии): отсутсвует       
Статус-код ответа: 200   
Тело ответа (при наличии): отсутсвует   

### 19. GET ​/api​/v1​/Books 
HTTP-метод: GET     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Books    
Заголовки запроса: "accept: text/plain; v=1.0"      
Тело запроса (при наличии): отсутсвует       
Статус-код ответа: 200   
Тело ответа (при наличии):   
```
[
  {
    "id": 1,
    "title": "Book 1",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 100,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2023-05-29T18:14:44.9414838+00:00"
  },
  {
    "id": 2,
    "title": "Book 2",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 200,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2023-05-28T18:14:44.941497+00:00"
  },
  {
    "id": 3,
    "title": "Book 3",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 300,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2023-05-27T18:14:44.941507+00:00"
  },
  {
    "id": 4,
    "title": "Book 4",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 400,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2023-05-26T18:14:44.9415167+00:00"
  },
  {
    "id": 5,
    "title": "Book 5",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 500,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2023-05-25T18:14:44.9415279+00:00"
  },
  {
    "id": 6,
    "title": "Book 6",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 600,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2023-05-24T18:14:44.941538+00:00"
  }
]
```

### 20. POST ​/api​/v1​/Books  Удачный
HTTP-метод: POST     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Authors/14543455454   
Заголовки запроса: "Content-Type: application/json; v=1.0"     
Тело запроса (при наличии):        
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-05-30T18:18:26.989Z"
}
```
Статус-код ответа: 200   
Тело ответа (при наличии):   
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-c4ec5e11b09cb044b514a4b86e4b89c4-893afb89afd1244c-00",
  "errors": {
    "id": [
      "The value '14543455454' is not valid."
    ]
  }
}
```
### 21. POST ​/api​/v1​/Books  Провальный
HTTP-метод: POST     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Authors/14543455454   
Заголовки запроса: "Content-Type: application/json; v=1.0"     
Тело запроса (при наличии):        
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-05-30T18:18:26.989Z"
}
```
Статус-код ответа: 400   
Тело ответа (при наличии):   
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-9e61787627c6004f98671ef56cbaf355-620ef5d8160a2245-00",
  "errors": {
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 17."
    ]
  }
}
```
### 22. GET ​/api​/v1​/Books​/{id}  Удачный
HTTP-метод: GET     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Books/12   
Заголовки запроса: "accept: text/plain; v=1.0"     
Тело запроса (при наличии): отсутсвует
Статус-код ответа: 200   
Тело ответа (при наличии):   
```
{
  "id": 12,
  "title": "Book 12",
  "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "pageCount": 1200,
  "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "publishDate": "2023-05-18T18:23:39.5217338+00:00"
}
```
### 23. GET ​/api​/v1​/Books​/{id}  Провальный
HTTP-метод: GET     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Books/124543634634   
Заголовки запроса: "accept: text/plain; v=1.0"     
Тело запроса (при наличии): отсутсвует
Статус-код ответа: 400   
Тело ответа (при наличии):   
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-296e581a54fe0049a54d86ee3ddf88d1-d9b8910231450445-00",
  "errors": {
    "id": [
      "The value '124543634634' is not valid."
    ]
  }
}
```

### 24. PUT ​/api​/v1​/Books​/{id} Удачный
HTTP-метод: PUT     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Books/0   
Заголовки запроса: "Content-Type: application/json; v=1.0"     
Тело запроса (при наличии): 
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-05-30T18:28:59.018Z"
}
```
Статус-код ответа: 200   
Тело ответа (при наличии):   
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-05-30T18:28:59.018Z"
}
```
### 25. PUT ​/api​/v1​/Books​/{id} Провальный
HTTP-метод: PUT     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Books/989898989898   
Заголовки запроса: "Content-Type: application/json; v=1.0"     
Тело запроса (при наличии): 
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-05-30T18:28:59.018Z"
}
```
Статус-код ответа: 400   
Тело ответа (при наличии):   
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-ba11727f4b813748a4ed35c2bd0cc2d6-4653c3b3ecd2124c-00",
  "errors": {
    "id": [
      "The value '989898989898' is not valid."
    ]
  }
}
```

### 26. DELETE ​/api​/v1​/Books​/{id}  Удачный
HTTP-метод: DELETE     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Books/1   
Заголовки запроса: "accept: */*"     
Тело запроса (при наличии): отсутсвует
Статус-код ответа: 200   
Тело ответа (при наличии): отсутсвует 

### 27. GET ​/api​/v1​/CoverPhotos 
HTTP-метод: GET     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos   
Заголовки запроса: "accept: text/plain; v=1.0"     
Тело запроса (при наличии): отсутсвует
Статус-код ответа: 200   
Тело ответа (при наличии): 
```
[
  {
    "id": 1,
    "idBook": 1,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
  },
  {
    "id": 2,
    "idBook": 2,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 2&w=250&h=350"
  },
  {
    "id": 3,
    "idBook": 3,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 3&w=250&h=350"
  },
  {
    "id": 4,
    "idBook": 4,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 4&w=250&h=350"
  },
  {
    "id": 5,
    "idBook": 5,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 5&w=250&h=350"
  },
  {
    "id": 6,
    "idBook": 6,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 6&w=250&h=350"
  }
]
```

### 28. POST ​/api​/v1​/CoverPhotos  Удачный
HTTP-метод: POST     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos   
Заголовки запроса: "Content-Type: application/json; v=1.0"     
Тело запроса (при наличии): 
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```
Статус-код ответа: 200   
Тело ответа (при наличии): 
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```

### 29. POST ​/api​/v1​/CoverPhotos  Провальный
HTTP-метод: POST     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos   
Заголовки запроса: "Content-Type: application/json; v=1.0"     
Тело запроса (при наличии): 
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```
Статус-код ответа: 400   
Тело ответа (при наличии): 
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-4327e838111507469ba0dd46f8da7f69-f3dcee0d0b758a40-00",
  "errors": {
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 19."
    ]
  }
}
```

### 30. GET ​/api​/v1​/CoverPhotos​/books​/covers​/{idBook}  Удачный
HTTP-метод: GET     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/1   
Заголовки запроса: "accept: text/plain; v=1.0"     
Тело запроса (при наличии): отсутсвует 
Статус-код ответа: 200   
Тело ответа (при наличии): 
```
[
  {
    "id": 1,
    "idBook": 1,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
  }
]
```

### 31. GET ​/api​/v1​/CoverPhotos​/books​/covers​/{idBook}  Провальный
HTTP-метод: GET     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/154545454545445   
Заголовки запроса: "accept: text/plain; v=1.0"     
Тело запроса (при наличии): отсутсвует 
Статус-код ответа: 400   
Тело ответа (при наличии): 
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-19e896a02e74804ba07031a8e2ae7ad5-0e6e139e418c3349-00",
  "errors": {
    "idBook": [
      "The value '154545454545445' is not valid."
    ]
  }
}
```

### 32. GET ​/api​/v1​/CoverPhotos​/{id} Успешный
HTTP-метод: GET     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/1   
Заголовки запроса: "accept: text/plain; v=1.0"     
Тело запроса (при наличии): отсутсвует 
Статус-код ответа: 200   
Тело ответа (при наличии): 
```
{
  "id": 1,
  "idBook": 1,
  "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
}
```

### 33. GET ​/api​/v1​/CoverPhotos​/{id} Провальный 
HTTP-метод: GET     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/1444444444444   
Заголовки запроса: "accept: text/plain; v=1.0"     
Тело запроса (при наличии): отсутсвует 
Статус-код ответа: 400   
Тело ответа (при наличии): 
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-7967e991e396df4789792afeb058f9fa-9f930b9351a24e48-00",
  "errors": {
    "id": [
      "The value '1444444444444' is not valid."
    ]
  }
}
```

### 34. PUT ​/api​/v1​/CoverPhotos​/{id} Удачный
HTTP-метод: PUT     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/1   
Заголовки запроса: "accept: text/plain; v=1.0"     
Тело запроса (при наличии): 
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```
Статус-код ответа: 200   
Тело ответа (при наличии): 
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```

### 35. PUT ​/api​/v1​/CoverPhotos​/{id} Провальный 
HTTP-метод: PUT     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/111111111111   
Заголовки запроса: "accept: text/plain; v=1.0"     
Тело запроса (при наличии): 
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```
Статус-код ответа: 400   
Тело ответа (при наличии): 
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-e663076c808c864fa7620bce5b8ecca6-11eb9a516342ca4d-00",
  "errors": {
    "id": [
      "The value '111111111111' is not valid."
    ]
  }
}
```

### 36. DELETE ​/api​/v1​/CoverPhotos​/{id} 
HTTP-метод: DELETE     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/1   
Заголовки запроса: "accept: */*"     
Тело запроса (при наличии): отсутсвует
Статус-код ответа: 200   
Тело ответа (при наличии): отсутсвует

### 37. GET ​/api​/v1​/Users 
HTTP-метод: GET     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Users   
Заголовки запроса:  "accept: text/plain; v=1.0"      
Тело запроса (при наличии): отсутсвует
Статус-код ответа: 200   
Тело ответа (при наличии): 
```
[
  {
    "id": 1,
    "userName": "User 1",
    "password": "Password1"
  },
  {
    "id": 2,
    "userName": "User 2",
    "password": "Password2"
  },
  {
    "id": 3,
    "userName": "User 3",
    "password": "Password3"
  },
  {
    "id": 4,
    "userName": "User 4",
    "password": "Password4"
  },
  {
    "id": 5,
    "userName": "User 5",
    "password": "Password5"
  },
  {
    "id": 6,
    "userName": "User 6",
    "password": "Password6"
  }
]
```
### 38. POST ​/api​/v1​/Users Удачный 
HTTP-метод: POST     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Users   
Заголовки запроса:  "Content-Type: application/json; v=1.0"       
Тело запроса (при наличии): 
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
Статус-код ответа: 200   
Тело ответа (при наличии): 
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```

### 39. POST ​/api​/v1​/Users Провальный 
HTTP-метод: POST     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Users   
Заголовки запроса:  "Content-Type: application/json; v=1.0"       
Тело запроса (при наличии): 
```
{
  "id": 85558585858858,
  "userName": "string",
  "password": "string"
}
```
Статус-код ответа: 400   
Тело ответа (при наличии): 
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-b1d3b92e02e78944ac1b4fbe26658bf7-dbacb012c76bbb42-00",
  "errors": {
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 20."
    ]
  }
}
```

### 40. GET ​/api​/v1​/Users​/{id} Удачный
HTTP-метод: GET     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Users/1   
Заголовки запроса:  "accept: */*"       
Тело запроса (при наличии): отсутсвует    
Статус-код ответа: 200   
Тело ответа (при наличии): 
```
{
  "id": 1,
  "userName": "User 1",
  "password": "Password1"
}
```

### 41. GET ​/api​/v1​/Users​/{id} Провальный
HTTP-метод: GET     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Users/14565464565465  
Заголовки запроса:  "accept: */*"       
Тело запроса (при наличии): отсутсвует    
Статус-код ответа: 400   
Тело ответа (при наличии):    
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-b43e74bef51f7a47ab70e8f0d4293561-d64a97144672d34c-00",
  "errors": {
    "id": [
      "The value '14565464565465' is not valid."
    ]
  }
}
```

### 42. PUT ​/api​/v1​/Users​/{id} Удачный
HTTP-метод: PUT     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Users/1  
Заголовки запроса:  "Content-Type: application/json; v=1.0"       
Тело запроса (при наличии): 
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
Статус-код ответа: 200   
Тело ответа (при наличии):    
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```

### 43. PUT ​/api​/v1​/Users​/{id} Провальный
HTTP-метод: PUT     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Users/098765436566  
Заголовки запроса: "Content-Type: application/json; v=1.0"       
Тело запроса (при наличии): 
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
Статус-код ответа: 400   
Тело ответа (при наличии):    
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-a301c7f3ade6374bbd6d567b8d070e34-db025d6185e27f47-00",
  "errors": {
    "id": [
      "The value '098765436566' is not valid."
    ]
  }
}
```

### 44. DELETE ​/api​/v1​/Users​/{id} 
HTTP-метод: DELETE     
Полный URL запрос: https://fakerestapi.azurewebsites.net/api/v1/Users/1   
Заголовки запроса: "accept: */*"     
Тело запроса (при наличии): отсутсвует
Статус-код ответа: 200   
Тело ответа (при наличии): отсутсвует