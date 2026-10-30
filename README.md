# Campus Library: GraphQL + MySQL

A small web app that lists authors with their books and lets you add a book.

**Stack:** HTML/CSS → GraphQL API (Node.js + Apollo Server) → MySQL

## Setup

1. Install Node.js and MySQL.
2. Create the database: run the SQL in `schema.sql` in MySQL.
3. Install libraries:
   ```
   npm install
   ```
4. Open `db.js` and put your MySQL root password in.
5. Start the API:
   ```
   node server.js
   ```
   It runs at http://localhost:4000/
6. In VS Code, right-click `public/index.html` and choose **Open with Live Server**.

## Example query

```graphql
query {
  authors {
    name
    country
    books { title year }
  }
}
```

## Project structure

```
Campus-Library/
  schema.sql      database and tables
  db.js           MySQL connection
  server.js       GraphQL schema and resolvers
  public/
    index.html    web page (query + mutation)
    style.css     styling
```

## Author

NEERAJ SHARMA
