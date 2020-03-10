# Routing Notes

## - REST vs Non REST

| Non Rest        | REST             | Action    |
| :-------------- | :--------------- | :-------- |
| /listAllLessons | /api/lessons     | GET       |
| /createLesson   | /api/lessons     | POST      |
| /deleteLesson   | /api/lessons/:id | DELETE    |
| /updateUser     | /api/users/:id   | PATCH/PUT |

## - Menu

- CommonJS modules (require/export).
- Express Router (break up a server in sub components).
- Different ways to read data from the client.
  - body --> req.body
  - query string --> req.query
  - URL parameter --> req.params
  -
- using sub-routes

## Requirement

- list all hubs
- add a hub
- update a hub
- remove a hub
- view hub messages
- post a message to a hub

## Data Access

- use `hubs-model.js` to talk to the database
  - find (query)
  - findById (id)
  - add (hub)
  - remove (id)
  - update (id, changes)
  - findHubMessages (hubId)
  - findMessageById (messageId)
  - addMessage (message)

**Everyone of those methods returns a promise**

## Basic Application Architecture

- UI layer/code.
- Business Logic layer/code.
- Database layer/code.

## Using Query String Parameters

https://www.google.com/
search
? -----> marks the beginning of the query string
source=hp -----> key/value pair
& -----> separates key/value pairs
ei=btFnXuPPGuiqggf5-qmAAg
&
q=mdn+query+string+parameters

```js
req.query = {
  source: hp,
  ei: btFnXuPPGuiqggf5 - qmAAg,
  q: mdn + query + string + parameters
};
```
