---
alias: ???
path: /docs/reference/simple-api/update-or-create-nodes
layout: REFERENCE
shorttitle: Update or create nodes
description: Updates fields of an existing node or create a new node in your GraphQL backend. The node fields will be updated according to the provided values.
simple_relay_twin: ???
tags:
  - simple-api
  - mutations
  - nodes
related:
  further:
    - wooghee1za
    - fasie2rahv
    - koo4eevun4
  more:
    - cahzai2eur
    - dah6aifoce
---

# Update or Create nodes with the Simple API

Updates [fields](!alias-teizeit5se) of an existing node of a certain [type](!alias-ij2choozae) specified by the `id` field. If the `id` field is an empty string `""`, a new node of the [type](!alias-ij2choozae) will be created. The node's fields will be updated according to the additionally provided values.

The query response can contain all fields of the updated or created node.

> Create a new node (by passing an id of `""`), and return the newly created `id`:

```graphql
---
endpoint: https://api.graph.cool/simple/v1/???
disabled: true
---
mutation {
  updateOrCreatePost(
    id: ""
    text: "This is the start of my biggest adventure!"
    published: true
  ) {
    id
  }
}
---
{
  "data": {
    "updatePost": {
      "id": "cixnen24p33lo0143bexvr52n",
      "text": "This is the start of my biggest adventure!",
      "published": true
    }
  }
}
```

> Update an existing node:

```graphql
---
endpoint: https://api.graph.cool/simple/v1/???
disabled: true
---
mutation {
  updateOrCreatePost(
    id: "cixnen24p33lo0143bexvr52n"
    text: "And so the adventure continues!"
    published: false
  ) {
    id
  }
}
---
{
  "data": {
    "updatePost": {
      "id": "cixnen24p33lo0143bexvr52n",
      "text": "And so the adventure continues!",
      "published": false
    }
  }
}
```
