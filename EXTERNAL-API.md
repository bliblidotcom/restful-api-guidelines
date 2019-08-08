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

## Sorting

```
/api/products?page=1&item_per_page=100&sort_by=firstName:asc,lastName:desc
```
