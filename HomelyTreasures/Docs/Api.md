# Homely Treasures API

- [Homely Treasures API](#homely-treasures-api)
  - [Create product](#create-product)
    - [Create product Request](#create-product-request)
    - [Create product Response](#create-product-response)
  - [Get product](#get-product)
    - [Get product Request](#get-product-request)
    - [Get product Response](#get-product-response)
  - [Update product](#update-product)
    - [Update product Request](#update-product-request)
    - [Update product Response](#update-product-response)
  - [Delete product](#delete-product)
    - [Delete product Request](#delete-product-request)
    - [Delete product Response](#delete-product-response)

## Create Product

### Create Product Request

```js
POST /products
```

```json
{
    "name": "Vanilla Scented Soap",
    "description": "Cold pressed vanilla scented soap",
    "createdDateTime": "2023-02-19T08:00:00",
    "price": "6",
    "quantity": "8"
}
```

### Create Product Response

```js
201 Created
```

```yml
Location: {{host}}/Products/{{id}}
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Vanilla Scented Soap",
    "description": "Cold pressed vanilla scented soap",
    "createdDateTime": "2023-02-19T08:00:00",
    "lastModifiedDateTime": "2023-02-19T16:00:00",
    "price": "6",
    "quantity": "8" 
}
```

## Get Product

### Get Product Request

```js
GET /products/{{id}}
```

### Get Product Response

```js
200 Ok
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Vanilla Scented Soap",
    "description": "Cold pressed vanilla scented soap",
    "createdDateTime": "2023-02-19T08:00:00",
    "lastModifiedDateTime": "2023-02-19T16:00:00",
    "price": "6",
    "quantity": "8"
}
```

## Update Product

### Update Product Request

```js
PUT /products/{{id}}
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Vanilla Scented Soap",
    "description": "Cold pressed vanilla scented soap",
    "createdDateTime": "2023-02-19T08:00:00",
    "price": "6",
    "quantity": "8"
}
```

### Update Product Response

```js
204 No Content
```

or

```js
201 Created
```

```yml
Location: {{host}}/Products/{{id}}
```

## Delete Product

### Delete Product Request

```js
DELETE /products/{{id}}
```

### Delete Product Response

```js
204 No Content
```