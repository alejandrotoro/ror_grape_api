# README

Following this tutorial:
Step 1: <https://medium.com/@clementrollon/build-a-basic-api-with-grape-api-grape-entity-part-1-5d5fa1cf38db>
Step 2: <https://medium.com/@clementrollon/build-a-basic-api-with-grape-api-grape-entity-part-2-25ed0d22dfb7>
Step 3: <https://medium.com/@clementrollon/build-a-basic-api-with-grape-api-grape-entity-part-3-c186dda08938>

## List grape routes

```bash
rails grape:routes
```

      GET  |  /api/:version/books(.json)            |  v1  |  Return list of books
      GET  |  /api/:version/books/:id(.json)        |  v1  |  Return a specific book
     POST  |  /api/:version/books/:id/flows(.json)  |  v1  |  Create a flow

## Routes

### List all books

<http://localhost:3000/api/v1/books>

### List a book

<http://localhost:3000/api/v1/books/1>

### Create flows

curl -i -X POST -H 'Content-Type: application/json' -d '{ "flow": { "newStock": 10, "previousStock": 12 } }' <http://localhost:3000/api/v1/books/1/flows>
