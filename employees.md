# GET
## /
```json
{
  "_embedded": {
    "employees": [
      {
        "githubId": 0,
        "username": "admin",
        "password": "$2a$10$NpegG0gF5bapL9ZYEFN5q.CCOL.Z.jz53edMY1YztGxPjafwN5B3W",
        "email": "sammi.fux@ordina.be",
        "firstName": "Sammi",
        "lastName": "Fux",
        "avatar": "https://media.licdn.com/media/AAEAAQAAAAAAAAVgAAAAJDRjNGE2ZWVkLTM3NzEtNDNhZC1hMDdiLTI3NmU4MGU5Mzk0Zg.jpg",
        "phone": "0469696969",
        "unit": null,
        "gender": null,
        "enabled": 1,
        "deleted": 0,
        "id": "fe81c22c-c818-41ce-ba02-a38504372b72",
        "_links": {
          "self": {
            "href": "http://104.40.147.238:8081/employees/admin"
          }
        }
      },
      "..."
    ]},
    "_links": {
      "first": {
        "href": "http://104.40.147.238:8081/employees?page=0&size=20"
      },
      "self": {
        "href": "http://104.40.147.238:8081/employees"
      },
      "next": {
        "href": "http://104.40.147.238:8081/employees?page=1&size=20"
      },
      "last": {
        "href": "http://104.40.147.238:8081/employees?page=3&size=20"
      }
    },
    "page": {
      "size": 20,
      "totalElements": 64,
      "totalPages": 4,
      "number": 0
  }
}

```
## /{username}
```json
{
  "githubId": 0,
  "username": "admin",
  "password": "$2a$10$NpegG0gF5bapL9ZYEFN5q.CCOL.Z.jz53edMY1YztGxPjafwN5B3W",
  "email": "sammi.fux@ordina.be",
  "firstName": "Sammi",
  "lastName": "Fux",
  "avatar": "https://media.licdn.com/media/AAEAAQAAAAAAAAVgAAAAJDRjNGE2ZWVkLTM3NzEtNDNhZC1hMDdiLTI3NmU4MGU5Mzk0Zg.jpg",
  "phone": "0469696969",
  "unit": null,
  "gender": null,
  "enabled": 1,
  "deleted": 0,
  "id": "fe81c22c-c818-41ce-ba02-a38504372b72",
  "_links": {
    "self": {
      "href": "http://104.40.147.238:8081/employees/admin"
    }
  }
}
```
## /search/findByRole?roleTitle=admin
```json
{
  "_embedded": {
    "employees": [
      {
        "githubId": 0,
        "username": "admin",
        "password": "$2a$10$NpegG0gF5bapL9ZYEFN5q.CCOL.Z.jz53edMY1YztGxPjafwN5B3W",
        "email": "sammi.fux@ordina.be",
        "firstName": "Sammi",
        "lastName": "Fux",
        "avatar": "https://media.licdn.com/media/AAEAAQAAAAAAAAVgAAAAJDRjNGE2ZWVkLTM3NzEtNDNhZC1hMDdiLTI3NmU4MGU5Mzk0Zg.jpg",
        "phone": "0469696969",
        "unit": null,
        "gender": null,
        "enabled": 1,
        "deleted": 0,
        "id": "fe81c22c-c818-41ce-ba02-a38504372b72",
        "_links": {
          "self": {
            "href": "http://104.40.147.238:8081/employees/admin"
          }
        }
      }],
      "_links": {
        "self": {
          "href": "http://104.40.147.238:8081/employees/search/findByRole"
        }
      },
      "page": {
        "size": 0,
        "totalElements": 2,
        "totalPages": 1,
        "number": 0
      }
    }
}
```

# POST
## /
* Should not be used

# PUT
## {username}

Input:

```json
{
"githubId": 0,
"username": "",
"email": "",
"firstName": "",
"lastName": "",
"avatar": "",
"roles": [ // Should be optional if rebased with latest version shadi
{"title": "admin"}
]
"phone": "",
"unit": "",
"gender": ""
}
```

# DELETE
## /{username}

* No body needed
