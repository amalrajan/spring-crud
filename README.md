# Spring CRUD

Foundation for implementing REST APIs using Spring with in-memory database PostgreSQL

## Cloning 
```
git clone https://github.com/amalrajan/spring-crud.git
cd spring-crud
./mvnw spring-boot:run
```

## Requests

### Get a list of Things
```
GET https://localhost:8080/
```

### Create a new Thing
```
POST http://localhost:8080/api/v1/student
Content-Type: application/json

{
    "name": "New Name",
    "email": "newname@gmail.com",
    "dob": "1999-12-17"
}
```

### Trash a Thing

#### Request

```
DELETE http://localhost:8080/api/v1/student/{id}
```

#### Response

```
DELETE http://localhost:8080/api/v1/student/1

HTTP/1.1 200 
Content-Length: 0
Date: Sat, 10 Jul 2021 14:26:08 GMT
Keep-Alive: timeout=60
Connection: keep-alive

<Response body is empty>

Response code: 200; Time: 215ms; Content length: 0 bytes
```

### Change a Thing

#### Request

```
PUT http://localhost:8080/api/v1/student/1?name={updatedName}&email={updatedEmail@gmail.com}
Content-Type: application/json
```

#### Response
```
PUT http://localhost:8080/api/v1/student/1?name=newName&email=changedEmail%40gmail.com

HTTP/1.1 200 
Content-Length: 0
Date: Sat, 10 Jul 2021 14:39:28 GMT
Keep-Alive: timeout=60
Connection: keep-alive

<Response body is empty>

Response code: 200; Time: 99ms; Content length: 0 bytes
```

