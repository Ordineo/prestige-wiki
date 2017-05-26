# GET
## /
```json
{
  "_embedded": {
    "endorsements": [
      {
        "granterUsername": "ChrisDeBruyne",
        "receiverUsername": "davedeg",
        "categories": [
          "Presentation",
          "Briefing"
        ],
        "endorsementLikes": [
          {
            "granterUsername": "Tyranwyn",
            "reason": "Amuzing",
            "created": "2017-05-24",
            "id": "45710e5e-16f9-4c63-9216-d86f872464d0",
            "_links": {
              "endorsement": {
                "href": "http://104.40.147.238:8082/endorsements/a2a48938-0e5a-402e-a7ac-0c9bb35c37cc"
              }
            }
          }
        ],
        "score": 1,
        "reason": "De presentatie was super duidelijk",
        "url": "https://www.ordina.be/",
        "created": "2017-05-24",
        "id": "a2a48938-0e5a-402e-a7ac-0c9bb35c37cc",
        "_links": {
          "self": {
            "href": "http://104.40.147.238:8082/endorsements/a2a48938-0e5a-402e-a7ac-0c9bb35c37cc"
          }
        }
      },
      "..."
      ]
    },
    "_links": {
      "self": {
        "href": "http://104.40.147.238:8082/endorsements"
      }
    },
    "page": {
      "size": 20,
      "totalElements": 6,
      "totalPages": 1,
      "number": 0
    }
}
```

## /{uuid}
```json
{
  "granterUsername": "ChrisDeBruyne",
  "receiverUsername": "davedeg",
  "categories": [
    "Presentation",
    "Briefing"
  ],
  "endorsementLikes": [
    {
      "granterUsername": "Tyranwyn",
      "reason": "Amuzing",
      "created": "2017-05-24",
      "id": "45710e5e-16f9-4c63-9216-d86f872464d0",
      "_links": {
        "endorsement": {
          "href": "http://104.40.147.238:8082/endorsements/a2a48938-0e5a-402e-a7ac-0c9bb35c37cc"
        }
      }
    }
  ],
  "score": 1,
  "reason": "De presentatie was super duidelijk",
  "url": "https://www.ordina.be/",
  "created": "2017-05-24",
  "id": "a2a48938-0e5a-402e-a7ac-0c9bb35c37cc",
  "_links": {
    "self": {
      "href": "http://104.40.147.238:8082/endorsements/a2a48938-0e5a-402e-a7ac-0c9bb35c37cc"
    }
  }
}
```

## /search/findByGranterUsername?username=ChrisDeBruyne
```json
{
  "_embedded": {
    "endorsements": [
      {
        "granterUsername": "ChrisDeBruyne",
        "receiverUsername": "davedeg",
        "categories": [
          "Presentation",
          "Briefing"
        ],
        "endorsementLikes": [
          {
            "granterUsername": "Tyranwyn",
            "reason": "Amuzing",
            "created": "2017-05-24",
            "id": "45710e5e-16f9-4c63-9216-d86f872464d0",
            "_links": {
              "endorsement": {
                "href": "http://104.40.147.238:8082/endorsements/a2a48938-0e5a-402e-a7ac-0c9bb35c37cc"
              }
            }
          }
        ],
        "score": 1,
        "reason": "De presentatie was super duidelijk",
        "url": "https://www.ordina.be/",
        "created": "2017-05-24",
        "id": "a2a48938-0e5a-402e-a7ac-0c9bb35c37cc",
        "_links": {
          "self": {
            "href": "http://104.40.147.238:8082/endorsements/a2a48938-0e5a-402e-a7ac-0c9bb35c37cc"
          }
        }
      }
    ]
  },
  "_links": {
    "self": {
      "href": "http://104.40.147.238:8082/endorsements/search/findByGranterUsername"
    }
  },
  "page": {
    "size": 20,
    "totalElements": 1,
    "totalPages": 1,
    "number": 0
  }
}
```

## /search/findByReceiverUsername?username=davedeg
```json
{
  "_embedded": {
    "endorsements": [
      {
        "granterUsername": "ChrisDeBruyne",
        "receiverUsername": "davedeg",
        "categories": [
          "Presentation",
          "Briefing"
        ],
        "endorsementLikes": [
          {
            "granterUsername": "Tyranwyn",
            "reason": "Amuzing",
            "created": "2017-05-24",
            "id": "45710e5e-16f9-4c63-9216-d86f872464d0",
            "_links": {
              "endorsement": {
                "href": "http://104.40.147.238:8082/endorsements/a2a48938-0e5a-402e-a7ac-0c9bb35c37cc"
              }
            }
          }
        ],
        "score": 1,
        "reason": "De presentatie was super duidelijk",
        "url": "https://www.ordina.be/",
        "created": "2017-05-24",
        "id": "a2a48938-0e5a-402e-a7ac-0c9bb35c37cc",
        "_links": {
          "self": {
            "href": "http://104.40.147.238:8082/endorsements/a2a48938-0e5a-402e-a7ac-0c9bb35c37cc"
          }
        }
      },
      {
        "granterUsername": "gurtjun",
        "receiverUsername": "davedeg",
        "categories": [
          "Coffee"
        ],
        "endorsementLikes": [],
        "score": 1,
        "reason": "Bedankt voor de goede koffie",
        "url": "https://www.google.be/",
        "created": "2017-05-24",
        "id": "5a97c460-f96d-4b7b-89a6-a824cbeedaea",
        "_links": {
          "self": {
            "href": "http://104.40.147.238:8082/endorsements/5a97c460-f96d-4b7b-89a6-a824cbeedaea"
          }
        }
      }
    ]
  },
  "_links": {
    "self": {
      "href": "http://104.40.147.238:8082/endorsements/search/findByReceiverUsername"
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
## /search/findByCategory?category=Presentation
```json
{
  "_embedded": {
    "endorsements": [
      {
        "granterUsername": "ChrisDeBruyne",
        "receiverUsername": "davedeg",
        "categories": [
          "Presentation",
          "Briefing"
        ],
        "endorsementLikes": [
          {
            "granterUsername": "Tyranwyn",
            "reason": "Amuzing",
            "created": "2017-05-24",
            "id": "45710e5e-16f9-4c63-9216-d86f872464d0",
            "_links": {
              "endorsement": {
                "href": "http://104.40.147.238:8082/endorsements/a2a48938-0e5a-402e-a7ac-0c9bb35c37cc"
              }
            }
          }
        ],
        "score": 1,
        "reason": "De presentatie was super duidelijk",
        "url": "https://www.ordina.be/",
        "created": "2017-05-24",
        "id": "a2a48938-0e5a-402e-a7ac-0c9bb35c37cc",
        "_links": {
          "self": {
            "href": "http://104.40.147.238:8082/endorsements/a2a48938-0e5a-402e-a7ac-0c9bb35c37cc"
          }
        }
      }
    ]
  },
  "_links": {
    "self": {
      "href": "http://104.40.147.238:8082/endorsements/search/findByCategory"
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

# POST
## /
```json
{
//    No granter required, added based on jwt token in backend
    "receiverUsername": "",
    "categories": [
      "",
      ""
    ],
    "score": 1,
    "reason": "",
    "url": ""
}
```

# PUT
## /{uuid}
```json
{
    "granterUsername": "",
    "receiverUsername": "",
    "categories": [
      "",
      ""
    ],
    "score": 1,
    "reason": "",
    "url": ""
}
```

# DELETE
## /{uuid}

* No input needed