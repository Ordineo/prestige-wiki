# GET
## /
```json
{
  "_embedded": {
    "categories": [
      {
        "name": "Presentation",
        "_links": {
          "self": {
            "href": "http://104.40.147.238:8082/categories/1"
          }
        }
      },
      {
        "name": "Email",
        "_links": {
          "self": {
            "href": "http://104.40.147.238:8082/categories/2"
          }
        }
      },
      {
        "name": "Coffee",
        "_links": {
          "self": {
            "href": "http://104.40.147.238:8082/categories/3"
          }
        }
      },
      {
        "name": "Briefing",
        "_links": {
          "self": {
            "href": "http://104.40.147.238:8082/categories/4"
          }
        }
      },
      {
        "name": "Workshop",
        "_links": {
          "self": {
            "href": "http://104.40.147.238:8082/categories/5"
          }
        }
      }
    ]
  },
  "_links": {
    "self": {
      "href": "http://104.40.147.238:8082/categories"
    }
  },
  "page": {
    "size": 20,
    "totalElements": 5,
    "totalPages": 1,
    "number": 0
  }
}
```

# POST
## /
Input:
```json
{
 "name": ""
}
```

# DELETE
## {id}
* No input required