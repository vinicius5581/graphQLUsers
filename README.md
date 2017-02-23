# Users

## heroku:
It contains only up to the content on Very basic using static data, because I haven't figure out how to run json server on a separate port on heroku yet. If you want to see the full version, clone the project and run either `npm run start` or `npm run dev`.

https://secure-cove-56926.herokuapp.com/graphql

## Commands:

### Run app

`npm run start`

### Run app dev
`npm run dev`

### Run Json Server

`npm run json:server`

#### REST Urls

- `localhost:3000/users`
- `localhost:3000/users/23`
- `localhost:3000/companies`
- `localhost:3000/companies/1`
- `localhost:3000/companies/1/users`


## npm dependencies (package.json):

### express
Handles incoming HTTP requests and make responses to send back to the user.

### express-graphql
Comparability layer between express and graphql.

### graphql
Library responsive to crawl through the data.

### lodash
Helper functions.

### Json Server
Mock data fake REST API

### GraphQL Queries Samples

```
{
  company(id: "1") {
  	name
    users {
      firstName
    }
  }
}
```

```
query findCompany {
  apple: company(id: "1") {
    ...companyDetails
  }
  google: company(id: "2") {
    ...companyDetails
  }
}

fragment companyDetails on Company {
  name
  users {
    firstName
  }
}
```

### GraphQL Mutations

```
mutation {
  addUser(firstName: "Stephen", age: 26) {
    id
    firstName
    age
  }
}
```
