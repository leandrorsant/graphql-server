# GraphQL Server

This is a GraphQL API which fetches data from an in-memory database to demonstrate what this library can do to reduce the amount of requests needed to get resourcers from a server.

# Getting started
Clone this repository:
```
git clone ...
```

Install dependencies:
```
npm i
```

Run server:
```
npm run devStart
```
This project doesn't have a frontend url, but it has a GraphiQL interface at (http://localhost:5000/graphql) once the server is running. You can use GraphiQL to test queries as demonstrated in the screenshots bellow.

# Query samples
List all books:
```
{
  books {
    id,
    name,
    authorId,
  }
}

```
List all Authors:
```
{
  authors {
    id,
    name
  }
}
```

Add a book:
```
mutation {
  addBook(name: "new book", authorId: 1) {
    id
    name
  }
}
```

Add an author:
```
mutation {
  addAuthor(name: "new author") {
    id
    name
  }
}
```

Update a book:
```
mutation {
  updateBook(id: 1, name:"new name", authorId:1) {
    id,
    name
  }
}
```

Update an author:
```
mutation {
  updateAuthor(id: 1, name:"new name") {
    id,
    name
  }
}
```

Remove a book:
```
mutation {
  removeBook(id: 1) {
    id
    name
  }
}
```
Remove an author:
```
mutation {
  removeAuthor(id: 1) {
    id
    name
  }
}
```

#screenshots
<img src="./screenshots/graphql-server-screenshot1.png?raw=true">
<img src="./screenshots/graphql-server-screenshot2.png?raw=true">

