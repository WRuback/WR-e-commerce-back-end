# E-Commerce Back End

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Table of Contents

- [E-Commerce Back End](#e-commerce-back-end)
  - [Table of Contents](#table-of-contents)
  - [Description](#description)
  - [Installation](#installation)
  - [Usage](#usage)
    - [Categories](#categories)
    - [Tags](#tags)
    - [Products](#products)
  - [Video Walkthrough](#video-walkthrough)
  - [Contributing](#contributing)
  - [Tests](#tests)
  - [License](#license)
  - [Questions](#questions)

## Description

A project for my bootcamp to create the database schema and API calls for an e-commerce website using `Sequelize` and `Express`. The database stores information on product categories, product tags to help sort the products, and the products themselves, with there price and current stock stored. The API let's you GET all of the categories, tags, and products, either all of them or a single one by ID, POST new categories, tags, and products, PUT/Update them by ID, and DELETE them by ID as well.

## Installation

To install, download the repository, and in the terminal, on the directory you placed the files in, run `npm install` to setup the application. Once that finishes, run `mysql -u root -p`, and the enter your mysql password. Then, run `source db/schema.sql`. This will setup the database. Next, close mysql shell by typing `exit`. Then, run `npm run seed` to setup the tables and seed the starter information. Then, run `npm start`. Your API will then be up and running.

## Usage

Once the program is running, you can access the API at http://localhost:3001. Here you can preform the following calls.

### Categories

- `GET` api/categories/ - Returns the list of categories and the products in them.
- `GET` api/categories/:id - Returns the category with the matching ID and the products in it.
- `POST` api/categories/ - Lets you add a new category. include `category_name` in the json to have it work.
- `PUT` api/categories/:id - Lets you update a category with the matching ID. include `category_name` in the json to have it work.
- `DELETE` api/categories/:id - Removes the Category with the matching ID. This will delete the products in this category as well.

### Tags

- `GET` api/tags/ - Returns the list of tags and the products tagged by them.
- `GET` api/tags/:id - Returns the tag with the matching ID and the products tagged by them.
- `POST` api/tags/ - Lets you add a new tag. include `tag_name` in the json to have it work.
- `PUT` api/tags/:id - Lets you update a tag with the matching ID. include `tag_name` in the json to have it work.
- `DELETE` api/tags/:id - Removes the tag with the matching ID.

### Products

- `GET` api/products/ - Returns the list of products and their category and tags.
- `GET` api/products/:id - Returns the product with the matching ID and their category and tags.
- `POST` api/products/ - Lets you add a new product. include `product_name`, `price`, `stock`, and `tagIds` (as an array) in the json to have it work.
- `PUT` api/products/:id - Lets you update a product with the matching ID. include `product_name`, `price`, `stock`, and `tagIds` (as an array) in the json to have it work.
- `DELETE` api/products/:id - Removes the product with the matching ID.

## Video Walkthrough

[Watch the walkthrough video here.]()

## Contributing

Anyone can fork this project and add features. However, all changes to the main section must be approved by the Admin.

## Tests

There are no testing procedures for this project.

## License

This project is licensed under a [MIT license](https://opensource.org/licenses/MIT).

## Questions

If you have any questions, please send them to [WRuback](https://github.com/WRuback) at wrubackdev@gmail.com with the heading "E-Commerce Back End Question".
