# Product API Testing with Postman

This project demonstrates API testing of a Product module using **Postman**, **Newman**, and **json-server**. It includes positive testing, end-to-end workflow testing, negative testing, schema validation, dynamic variable handling, and Newman report generation.

## 📚 Project Overview

The purpose of this project is to test REST API endpoints for product management. The project covers CRUD operations and validates both expected and unexpected scenarios.

## Tools Used

- Postman
- Newman
- json-server
- Node.js
- Microsoft Excel

## API Endpoints Tested

- `GET /products`
- `GET /products/:id`
- `POST /products`
- `PUT /products/:id`
- `DELETE /products/:id`

## Test Structure

### Positive Tests
- `TC01_GET_All_Products`
- `TC02_GET_Product_By_Valid_ID`

### End-to-End Workflow Tests
- `TC03_POST_Create_Product_Valid_Data`
- `TC04_GET_Created_Product_By_Dynamic_ID`
- `TC05_PUT_Update_Created_Product`
- `TC06_DELETE_Created_Product`
- `TC11_GET_Deleted_Product_Verification`

### Negative Tests
- `TC07_GET_Product_By_Invalid_ID`
- `TC08_POST_Create_Product_Missing_Name`
- `TC09_POST_Create_Product_Invalid_Price_Type`
- `TC10_DELETE_Product_Invalid_ID`

## Features

- CRUD operation testing
- Status code validation
- JSON response validation
- JSON schema validation
- Dynamic variable handling using Postman variables
- End-to-end workflow testing
- Negative testing
- Newman CLI execution
- Newman HTML report generation

## Request Flow

1. Get all products
2. Get product by valid ID
3. Create new product
4. Save created product ID dynamically
5. Get created product using saved ID
6. Update created product
7. Delete created product
8. Verify deleted product is no longer available

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
5. Run with Newman CLI
   Bash - newman run "Product_API_Testing.postman_collection.json" --env-var "baseURL=http://localhost:3000" -r cli
6. Generate Newman HTML Report
   Bash - newman run "Product_API_Testing.postman_collection.json" --env-var "baseURL=http://localhost:3000" -r "cli,htmlextra" --reporter-htmlextra-export "newman-report.html"


## Files Included
- db.json
- Product_API_Testing.postman_collection.json
- Product_Environment.postman_environment.json
- Product API Test Cases.xlsx
- newman-report.html
- README.md

## Screenshorts
<img width="558" height="564" alt="Newman CLI result" src="https://github.com/user-attachments/assets/74589120-5f6d-427b-af20-15df802eab97" />
<img width="960" height="479" alt="Test Case Report" src="https://github.com/user-attachments/assets/be105738-8570-4e57-966c-c9f44810f18e" />
<img width="292" height="388" alt="Collection structure" src="https://github.com/user-attachments/assets/c9deff6d-20a1-4fc7-89f3-3d1ab175c836" />
<img width="1359" height="682" alt="Newman HTML report" src="https://github.com/user-attachments/assets/99774510-a803-4f46-918e-efe31e060dfc" />
<img width="1107" height="664" alt="Postman runner all-pass result" src="https://github.com/user-attachments/assets/0aefca27-2bb6-47ce-ac29-30be6447f8fd" />


## Future Improvements
- Add authentication-based API testing
- Add more business rule validations
- Add additional modules such as Users or Orders
- Integrate GitHub Actions for automated test execution
- 
## Author
Abdullah Al Mahmud Joy
