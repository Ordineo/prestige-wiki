# GET
## /

```json
{
  "_embedded": {
    "roles": [
      {
        "title": "admin",
        "_links": {
          "self": {
            "href": "http://104.40.147.238:8081/roles/admin"
          },
          "employees": [
            {
              "href": "http://104.40.147.238:8081/employees/admin"
            },
            {
              "href": "http://104.40.147.238:8081/employees/Tyranwyn"
            }
          ]
        }
      }
    ]
  },
  "_links": {
    "self": {
      "href": "http://104.40.147.238:8081/roles"
    }
  },
  "page": {
    "size": 0,
    "totalElements": 1,
    "totalPages": 1,
    "number": 0
  }
}
```

#POST
## /
Input:
```json
{
  "title": ""
}
```

# DELETE
## /{title}

* No input required