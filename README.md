# Farm Stand CRUD

A simple product management web application built with **Node.js, Express, MongoDB, Mongoose, and EJS**.

The application demonstrates the core **CRUD (Create, Read, Update, Delete)** workflow for farm-stand products, with filtering by product category.

## Features

- View all products
- Filter products by category
- Add a new product
- View product details
- Edit an existing product
- Delete a product
- Server-side rendered pages using EJS
- MongoDB database integration using Mongoose
- Form method overriding for PUT and DELETE requests
- Mongoose validation for product name, price, and category

## Tech Stack

- **Backend:** Node.js, Express
- **Database:** MongoDB
- **ODM:** Mongoose
- **Templating:** EJS
- **HTTP Method Override:** method-override

## Product Model

Each product contains:

- `name` – required string
- `price` – required number, minimum `0`
- `category` – `fruit`, `vegetable`, or `dairy`

## CRUD Routes

| Method | Route | Purpose |
|---|---|---|
| GET | `/products` | Display all products / filter by category |
| GET | `/products/new` | Display product creation form |
| POST | `/products` | Create a new product |
| GET | `/products/:id` | Display one product |
| GET | `/products/:id/edit` | Display edit form |
| PUT | `/products/:id` | Update a product |
| DELETE | `/products/:id` | Delete a product |

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/farm-stand-crud.git
cd farm-stand-crud
```

### 2. Install dependencies

```bash
npm install
```

### 3. Start MongoDB

This project currently connects to a local MongoDB instance using:

```text
mongodb://127.0.0.1:27017/farmStand
```

Make sure MongoDB is running on your computer before starting the application.

### 4. Start the application

```bash
node index.js
```

The server runs on:

```text
http://localhost:3000
```

Open the products page at:

```text
http://localhost:3000/products
```

## Seed Sample Products

The project includes a `seeds.js` file containing sample farm-stand products.

Run it with:

```bash
node seeds.js
```

This inserts sample products such as vegetables, fruits, and dairy items into the MongoDB database.

## Project Structure

```text
farm-stand-crud/
├── models/
│   └── product.js
├── views/
│   └── products/
│       ├── index.ejs
│       ├── new.ejs
│       ├── show.ejs
│       └── edit.ejs
├── index.js
├── seeds.js
├── package.json
├── package-lock.json
├── .gitignore
└── README.md
```

## What I Learned

- Building an Express server
- Connecting a Node.js application to MongoDB with Mongoose
- Defining Mongoose schemas and models
- Implementing CRUD operations
- Using EJS for server-side rendering
- Handling form submissions with Express
- Using `method-override` for PUT and DELETE requests
- Validating database input with Mongoose
- Organizing a basic full-stack Node.js application

## Future Improvements

- Add authentication and authorization
- Add product images
- Add search and sorting
- Add pagination
- Improve UI styling and responsiveness
- Add centralized error handling
- Move the MongoDB connection string to an environment variable
- Deploy the application online

## License

This project is licensed under the MIT License.
