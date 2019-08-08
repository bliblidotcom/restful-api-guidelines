# Blibli External RESTful API Guidelines

## Response

```json
{
  "code" : 200,
  "status" : "OK",
  "data" : {
     "id" : "sample id"
  }
}
```

```json
{
  "code" : 200,
  "status" : "OK",
  "data" : [
    {
      "id" : "1",
      "name" : "Product 1"
    },
    {
      "id" : "1",
      "name" : "Product 1"
    }
  ]
}
```

## Error

```json
{
  "code" : 200,
  "status" : "OK",
  "errors" : {
    "email" : [
      "NotValid"
    ],
    "description" : [
      "NotValid",
      "TooLarge"
    ]
  }
}
```

## Paging 

```
/api/products?page=1&item_per_page=100
```

```json
```json
{
  "code" : 200,
  "status" : "OK",
  "data" : [
    {
      "id" : "1",
      "name" : "Product 1"
    },
    {
      "id" : "1",
      "name" : "Product 1"
    }
  ],
  "paging" : {
    "page" : 1,
    "total_page" : 100,
    "item_per_page" : 100,
    "total_item" : 10000
  }
}
```
```

## Sorting

```
/api/products?sort_by=firstName:asc,lastName:desc
```
