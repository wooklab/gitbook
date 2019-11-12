---
description: ElasticSearch Alias 변경하기
---

# ElasticSearch Alias

### Alias 변경하기

#### URI
```http
/_aliases
```

#### Json Query
```json
{
  "actions": [
    {
      "remove": {
        "index": "wmp2.0_search_set2",
        "alias": "dlv"
      }
    },
    {
      "add": {
        "index": "wmp2.0_search_set1",
        "alias": "dlv"
      }
    }
  ]
}
```
