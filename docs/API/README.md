# Bookstore API Documentation


### Endpoint: GET `/`

This endpoint retrieves a list of all bookstores.

#### Request

- Method: GET
- Route: `/`

#### Response

- Status Code 200 (OK) on success.

##### Response Body

- An array of objects representing bookstores.

- Status Code 404 (Not Found) if no bookstores are found.

##### Response Body

- `error` (string): "Wax bookstore majiriran"

## Get a Specific Bookstore

### Endpoint: GET `/:id`

This endpoint retrieves a specific bookstore by its ID.

#### Request

- Method: GET
- Route: `/:id`

##### Request Parameters

- `id` (number): The ID of the bookstore to retrieve.

#### Response

- Status Code 200 (OK) on success.

##### Response Body

- An object representing the requested bookstore.

- Status Code 404 (Not Found) if the requested bookstore does not exist.

##### Response Body

- `error` (string): "wax book mahayo"

## Create a New Bookstore

### Endpoint: POST `/`

This endpoint allows the creation of a new bookstore.

#### Request

- Method: POST
- Route: `/`

##### Request Body

- `name` (string): The name of the bookstore.
- `location` (string): The location of the bookstore.

#### Response

- Status Code 200 (OK) on success.

##### Response Body

- `message` (string): "Bookstore created successfully"
- `bookstore` (object): The details of the created bookstore.

- Status Code 404 (Not Found) if the bookstore creation fails.

##### Response Body

- `error` (string): "Bookstore not found"

## Update a Bookstore

### Endpoint: PUT `/:id`

This endpoint allows the updating of an existing bookstore by its ID.

#### Request

- Method: PUT
- Route: `/:id`

##### Request Parameters

- `id` (number): The ID of the bookstore to update.

##### Request Body

- `name` (string): The updated name of the bookstore.
- `location` (string): The updated location of the bookstore.

#### Response

- Status Code 200 (OK) on success.

##### Response Body

- An object representing the updated bookstore.

- Status Code 404 (Not Found) if the requested bookstore does not exist.

##### Response Body

- `message` (string): "mahelin bookstore"

## Delete a Bookstore

### Endpoint: DELETE `/:id`

This endpoint allows the deletion of a specific bookstore by its ID.

#### Request

- Method: DELETE
- Route: `/:id`

##### Request Parameters

- `id` (number): The ID of the bookstore to delete.

#### Response

- Status Code 200 (OK) on successful deletion.

##### Response Body

- `message` (string): "Bookstore deleted"

- Status Code 404 (Not Found) if the requested bookstore does not exist.

##### Response Body

- `message` (string): "Bookstore not found"

- Status Code 500 (Internal Server Error) if deletion fails.

##### Response Body

- `message` (string): "Failed to delete bookstore"



# Authentication API Documentation

This documentation provides an overview of two API endpoints for user authentication: **signup** and **login**.

## Signup

### Endpoint: POST `/signup`

This endpoint allows users to create a new owner account. Users need to provide their name, email, and password.

#### Request

- Method: POST
- Route: `/signup`

##### Request Body

- `name` (string): The owner's name.
- `email` (string): The owner's email.
- `password` (string): The owner's password.

#### Response

- Status Code 201 (Created) on success.

##### Response Body

- `message` (string): "Owner created successfully"
- `owner` (object): The owner's details, including their ID, name, and email.

- Status Code 404 (Not Found) if an owner with the provided email already exists.

##### Response Body

- `message` (string): "Owner already exists"

- Status Code 500 (Internal Server Error) on any unexpected errors.

##### Response Body

- `message` (string): "Something went wrong"
- `error` (string): A description of the error.

## Login

### Endpoint: POST `/login`

This endpoint allows owners to log in to their accounts by providing their email and password.

#### Request

- Method: POST
- Route: `/login`

##### Request Body

- `email` (string): The owner's email.
- `password` (string): The owner's password.

#### Response

- Status Code 200 (OK) on successful login.

##### Response Body

- `message` (string): "Owner logged in successfully"
- `token` (string): A JSON Web Token (JWT) used for authentication.

- Status Code 404 (Not Found) if no owner is found with the provided email.

##### Response Body

- `message` (string): "Owner not found"

- Status Code 401 (Unauthorized) if the provided password is incorrect.

##### Response Body

- `message` (string): "Invalid credentials"

- Status Code 500 (Internal Server Error) on any unexpected errors.

##### Response Body

- `message` (string): "Something went wrong"
- `error` (string): A description of the error.

# Author API Documentation

This documentation outlines the API endpoints for managing authors, including retrieving, creating, updating, and deleting authors. The API endpoints are as follows:

## List All Authors

### Endpoint: GET `/`

This endpoint retrieves a list of all authors.

#### Request

- Method: GET
- Route: `/`

#### Response

- Status Code 200 (OK) on success.

##### Response Body

- An array of objects representing authors.

- Status Code 404 (Not Found) if no authors are found.

##### Response Body

- `error` (string): "wax authors majiran"

## Get a Specific Author

### Endpoint: GET `/:id`

This endpoint retrieves a specific author by their ID.

#### Request

- Method: GET
- Route: `/:id`

##### Request Parameters

- `id` (number): The ID of the author to retrieve.

#### Response

- Status Code 200 (OK) on success.

##### Response Body

- An object representing the requested author.

- Status Code 404 (Not Found) if the requested author does not exist.

##### Response Body

- `error` (string): "wax author mahayo"

## Create a New Author

### Endpoint: POST `/`

This endpoint allows the creation of a new author.

#### Request

- Method: POST
- Route: `/`

##### Request Body

- `name` (string): The name of the author.

#### Response

- Status Code 200 (OK) on success.

##### Response Body

- `message` (string): "Author created successfully"
- `author` (object): The details of the created author.

- Status Code 404 (Not Found) if author creation fails.

##### Response Body

- `error` (string): "Authors not found"

## Update an Author

### Endpoint: PUT `/:id`

This endpoint allows the updating of an existing author by their ID.

#### Request

- Method: PUT
- Route: `/:id`

##### Request Parameters

- `id` (number): The ID of the author to update.

##### Request Body

- `name` (string): The updated name of the author.

#### Response

- Status Code 200 (OK) on success.

##### Response Body

- An object representing the updated author.

- Status Code 404 (Not Found) if the requested author does not exist.

##### Response Body

- `message` (string): "mahelin author"

## Delete an Author

### Endpoint: DELETE `/:id`

This endpoint allows the deletion of a specific author by their ID.

#### Request

- Method: DELETE
- Route: `/:id`

##### Request Parameters

- `id` (number): The ID of the author to delete.

#### Response

- Status Code 200 (OK) on successful deletion.

##### Response Body

- `message` (string): "Author deleted"

- Status Code 404 (Not Found) if the requested author does not exist.

##### Response Body

- `message` (string): "Author not found"

- Status Code 500 (Internal Server Error) if deletion fails.

##### Response Body

- `message` (string): "Failed to delete author"


# Book API Documentation



### Endpoint: GET `/`

This endpoint retrieves a list of all books.

#### Request

- Method: GET
- Route: `/`

#### Response

- Status Code 200 (OK) on success.

##### Response Body

- An array of objects representing books.

- Status Code 404 (Not Found) if no books are found.

##### Response Body

- `error` (string): "wax book majiran"

## Get a Specific Book

### Endpoint: GET `/:id`

This endpoint retrieves a specific book by its ID.

#### Request

- Method: GET
- Route: `/:id`

##### Request Parameters

- `id` (number): The ID of the book to retrieve.

#### Response

- Status Code 200 (OK) on success.

##### Response Body

- An object representing the requested book.

- Status Code 404 (Not Found) if the requested book does not exist.

##### Response Body

- `error` (string): "wax book mahayo"

## Create a New Book

### Endpoint: POST `/`

This endpoint allows the creation of a new book.

#### Request

- Method: POST
- Route: `/`

##### Request Body

- `title` (string): The title of the book.
- `price` (number): The price of the book.
- `image` (string): The image URL of the book.

#### Response

- Status Code 201 (Created) on success.

##### Response Body

- An object representing the created book.

- Status Code 404 (Not Found) if the book creation fails.

##### Response Body

- `message` (string): "book not found"

## Update a Book

### Endpoint: PUT `/:id`

This endpoint allows the updating of an existing book by its ID.

#### Request

- Method: PUT
- Route: `/:id`

##### Request Parameters

- `id` (number): The ID of the book to update.

##### Request Body

- `title` (string): The updated title of the book.
- `price` (number): The updated price of the book.
- `image` (string): The updated image URL of the book.

#### Response

- Status Code 200 (OK) on success.

##### Response Body

- An object representing the updated book.

- Status Code 404 (Not Found) if the requested book does not exist.

##### Response Body

- `message` (string): "mahelin book"

## Delete a Book

### Endpoint: DELETE `/:id`

This endpoint allows the deletion of a specific book by its ID.

#### Request

- Method: DELETE
- Route: `/:id`

##### Request Parameters

- `id` (number): The ID of the book to delete.

#### Response

- Status Code 200 (OK) on successful deletion.

##### Response Body

- `message` (string): "book deleted"

- Status Code 404 (Not Found) if the requested book does not exist.

##### Response Body

- `message` (string): "book not found"

- Status Code 500 (Internal Server Error) if deletion fails.

##### Response Body

- `message` (string): "Failed to delete book"

## Authentication

Authentication middleware can be applied to the "Create a New Book" (`POST /`) endpoint using the `autenticate` middleware. Ensure proper authentication handling as required by your application.

---




