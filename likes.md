# GET
## /
```json
{
  "_embedded": {
    "endorsementLikes": [
      {
        "granterUsername": "Tyranwyn",
        "reason": "Cuz i liek diz",
        "created": "2017-05-24",
        "id": "b1347ee6-89b9-43ab-a499-4d545c99be66",
        "_links": {
          "self": {
            "href": "http://104.40.147.238:8082/likes/b1347ee6-89b9-43ab-a499-4d545c99be66"
          }
        }
      },
      {
        "granterUsername": "DavyDeRaeve",
        "reason": "Cuz i liek diz too",
        "created": "2017-05-24",
        "id": "03d4397e-a796-41eb-833e-8174e29d71dc",
        "_links": {
          "self": {
            "href": "http://104.40.147.238:8082/likes/03d4397e-a796-41eb-833e-8174e29d71dc"
          }
        }
      },
      {
        "granterUsername": "bartcleven",
        "reason": "Cuz i liek diz three",
        "created": "2017-05-24",
        "id": "b5b76593-65b2-4f5d-81e8-652caf0f07cc",
        "_links": {
          "self": {
            "href": "http://104.40.147.238:8082/likes/b5b76593-65b2-4f5d-81e8-652caf0f07cc"
          }
        }
      },
      {
        "granterUsername": "AnthonySlabinck",
        "reason": "Cuz i liek diz four",
        "created": "2017-05-24",
        "id": "d74e818e-2a58-4480-864f-6b2d9a01170c",
        "_links": {
          "self": {
            "href": "http://104.40.147.238:8082/likes/d74e818e-2a58-4480-864f-6b2d9a01170c"
          }
        }
      },
      {
        "granterUsername": "Tyranwyn",
        "reason": "Amuzing",
        "created": "2017-05-24",
        "id": "45710e5e-16f9-4c63-9216-d86f872464d0",
        "_links": {
          "self": {
            "href": "http://104.40.147.238:8082/likes/45710e5e-16f9-4c63-9216-d86f872464d0"
          }
        }
      }
    ]
  },
  "_links": {
    "self": {
      "href": "http://104.40.147.238:8082/likes"
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
## /search/findByGranterUsername?username=Tyranwyn
```json
{
  "_embedded": {
    "endorsementLikes": [
      {
        "granterUsername": "Tyranwyn",
        "reason": "Cuz i liek diz",
        "created": "2017-05-24",
        "id": "b1347ee6-89b9-43ab-a499-4d545c99be66",
        "_links": {
          "self": {
            "href": "http://104.40.147.238:8082/likes/b1347ee6-89b9-43ab-a499-4d545c99be66"
          }
        }
      },
      {
        "granterUsername": "Tyranwyn",
        "reason": "Amuzing",
        "created": "2017-05-24",
        "id": "45710e5e-16f9-4c63-9216-d86f872464d0",
        "_links": {
          "self": {
            "href": "http://104.40.147.238:8082/likes/45710e5e-16f9-4c63-9216-d86f872464d0"
          }
        }
      }
    ]
  },
  "_links": {
    "self": {
      "href": "http://104.40.147.238:8082/likes/search/findByGranterUsername"
    }
  },
  "page": {
    "size": 20,
    "totalElements": 2,
    "totalPages": 1,
    "number": 0
  }
}
```
## /search/findByEndorsementUuid
Not yet implemented

# POST
## /
Input
```json
{
    "granterUsername": "Tyranwyn",
    "reason": "Cuz i liek diz",
    "created": "2017-05-24"
}
```