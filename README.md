# Product API Testing with Postman

This is a beginner API testing project built using Postman and json-server.

## Tools Used
- Postman
- json-server
- Node.js

## API Endpoints Tested
- GET /products
- GET /products/:id
- POST /products
- PUT /products/:id
- DELETE /products/:id

## Features
- CRUD operation testing
- Status code validation
- JSON response validation
- Dynamic ID handling using Postman variables

## How to Run
1. Install json-server
2. Run:
   json-server --watch db.json --port 3000
3. Import the Postman collection
4. Run the requests in Postman

## Project Flow
1. Get all products
2. Get product by fixed ID
3. Create new product
4. Save created product ID
5. Get created product by dynamic ID
6. Update created product
7. Delete created product