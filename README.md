# E-Commerce Back End

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

## Description
This application is the back end for an e-commerce site. It assists shop owners and employees with keeping track of their products. It utilizes a MySQL database that uses Sequelize to interact with it.

## Installation
1. Download the repository by running `git clone git@github.com:graceee96/ecommerce-backend.git` in the command line interface.
    * Alternative: run `git clone https://github.com/graceee96/ecommerce-backend.git` in the command line interface

2. Run `npm init -y` in the command line interface to create a ```package.json```
3. Install the following dependencies to run the application
    * mysql2: `npm i mysql2`
    * express: `npm i express`
    * dotenv: `npm i dotenv`
    * sequelize: `npm i sequelize`

## Usage
To start, create the database in MySQL Workbench by running: 
```
DROP DATABASE IF EXISTS ecommerce_db;
CREATE DATABASE ecommerce_db;
```
In the command line interface, add data into your database by running `node seeds/index.js`. After running this code, your database is seeded and ready to be interacted with.

Start your server by running `node server.js`.

In Insomnia, data can be created, read, updated, and deleted using the correct routes:

| Function | URL                | Action                    | Example URL | Example Request Body |
| :---     | :---               | :---                      | :---    | :--- |
| GET      | api/categories     | Returns all category data | n/a     | none |
| GET      | api/products       | Returns all product data  | n/a     | none |
| GET      | api/tags           | Returns all tag data      | n/a     | none |
| GET      | api/categories/:id | Returns a single category data with the specified ID | api/categories/1 | none |
| GET      | api/products/:id   | Returns a single product data with the specified ID  | api/products/2   | none |
| GET      | api/tags/:id       | Returns a single tag data with the specified ID      | api/tags/3       | none |
| POST     | api/categories     | Create a new category data | n/a     | `{ "category_name": "Jeans" }` |
| POST     | api/products       | Create a new product data  | n/a     | `{ "product_name": "Drafting Table Lamp", "price": 76.00, "stock": 15, "tagIds": [1, 2] }` |
| POST     | api/tags           | Create a new tag data      | n/a     | `{ "tag_name": "pink" }` |
| PUT      | api/categories/:id | Updates a single category data with the specified ID | api/categories/1 | `{ "category_name": "Silk Scarf" }` |
| PUT      | api/products/:id   | Updates a single product data with the specified ID  | api/products/2   | `{ "product_name": "Floral Pillowcase", "price": 95.00, "stock": 20, "tagIds": [4, 5] }` |
| PUT      | api/tags/:id       | Updates a single tag data with the specified ID      | api/tags/3       | `{ "tag_name": "red" }` |
| DELETE      | api/categories/:id | Deletes a single category data with the specified ID | api/categories/1 | none |
| DELETE      | api/products/:id   | Deletes a single product data with the specified ID  | api/products/2   | none |
| DELETE      | api/tags/:id       | Deletes a single tag data with the specified ID      | api/tags/3       | none |

### Link to video walkthrough
https://drive.google.com/file/d/1MsBbQnds28ekFjn4Sz5wjjhbkQzCHP-1/view?usp=sharing

## Credits

### Special Thanks
Made with help from Bryan Swarthout, Shawn Tschoepe, Scott McAnally (tutor).

## License
This repository is licensed under the [MIT License](https://opensource.org/licenses/MIT).