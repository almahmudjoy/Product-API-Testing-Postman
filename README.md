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

## Request Flow
1. Get all products
2. Get product by fixed ID
3. Create new product
4. Save created product ID dynamically
5. Get created product using saved ID
6. Update created product
7. Delete created product

## Sample Product Data
```json
{
  "name": "Sugar",
  "price": 90,
  "category": "Grocery"
} 
```
## How to Run
1. Install json-server
2. Run the server:

- json-server --watch db.json --port 3000

3. Import the Postman collection
4. Run the requests in Postman Collection Runner

## Files Included
- db.json
- Product API Testing.postman_collection.json
- README.md

## Future Improvements
- Add negative test cases
- Add more assertions
- Add Newman HTML report
- Add screenshots of test execution

## Author

"Abdullah Al Mahmud Joy"
