## To run
- `npm install` to install dependencies
- `npm start` to start the server on port 3000
- `npm test` to run test suite (server should be running simultaneously)

## About
Using `express` with `body-parser` to do routing.
Using `sequelize` with `sqlite3` to query the database.
This build is bare bones to get a working API out and is basically just many express routes that each do a SQL query and return the results, if any. There is a single test for each route that query's the database and passes if it returns 200. With more time I would probably implement better testing as right now we aren't checking the database for changes, just that the routes are succesful.

## Users table API
* GET    `/api/user`        - all users
* GET    `api/user/:id`     - get user by id
* POST   `/api/user`        - post new user from body { name }
* PUT    `api/user/:id`     - update user by id 
* DELETE `api/user/:id`     - delete user by id 

## Items table API
* GET    `/api/item`        - all items
* GET    `api/item/:id`     - get item by id
* POST   `/api/item`        - post new item from body { name }
* PUT    `api/item/:id`     - update item by id 
* DELETE `api/item/:id`     - delete item by id 

## Orders table API
* GET    `/api/order`        - all orders
* GET    `api/order/:id`     - get order by id
* POST   `/api/order`        - post new order from body { user_id }
* PUT    `api/order/:id`     - update order by id 
* DELETE `api/order/:id`     - delete order by id 

## Order_items table API
* GET    `/api/order_item`                    - all order_items
* GET    `api/order_item/order/:order_id`     - get order_items by order_id
* GET    `api/order_item/item/:item_id`     - get order_items by item_id
* POST   `/api/order_item`                  - post new order_item from body { order_id, item_id }
* DELETE `api/order_item/:order_id`         - delete by order_id 

