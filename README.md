# 🛒 Product API Testing with Postman

<p align="center">
  <img src="https://img.shields.io/badge/Postman-API%20Testing-orange?style=for-the-badge&logo=postman" />
  <img src="https://img.shields.io/badge/Newman-Test%20Runner-green?style=for-the-badge&logo=postman" />
  <img src="https://img.shields.io/badge/json--server-Mock%20API-blue?style=for-the-badge&logo=json" />
  <img src="https://img.shields.io/badge/Node.js-Backend%20Support-brightgreen?style=for-the-badge&logo=node.js" />
  <img src="https://img.shields.io/badge/Status-All%20Tests%20Passing-success?style=for-the-badge" />
</p>

---

## 📌 Project Overview

This project demonstrates **API testing** of a **Product module** using **Postman**, **Newman**, and **json-server**.  
It covers:

- ✅ Positive testing
- ✅ End-to-end workflow testing
- ✅ Negative testing
- ✅ JSON schema validation
- ✅ Dynamic variable handling
- ✅ Newman CLI execution
- ✅ Newman HTML report generation

The main goal of this project is to validate CRUD operations for product management APIs and ensure both expected and unexpected scenarios are handled correctly.

---

## 🧰 Tools Used

- **Postman**
- **Newman**
- **json-server**
- **Node.js**
- **Microsoft Excel**

---

## 🌐 API Endpoints Tested

- `GET /products`
- `GET /products/:id`
- `POST /products`
- `PUT /products/:id`
- `DELETE /products/:id`

---

## 🧪 Test Structure

### ✅ Positive Tests
- `TC01_GET_All_Products`
- `TC02_GET_Product_By_Valid_ID`

### 🔄 End-to-End Workflow Tests
- `TC03_POST_Create_Product_Valid_Data`
- `TC04_GET_Created_Product_By_Dynamic_ID`
- `TC05_PUT_Update_Created_Product`
- `TC06_DELETE_Created_Product`
- `TC11_GET_Deleted_Product_Verification`

### ❌ Negative Tests
- `TC07_GET_Product_By_Invalid_ID`
- `TC08_POST_Create_Product_Missing_Name`
- `TC09_POST_Create_Product_Invalid_Price_Type`
- `TC10_DELETE_Product_Invalid_ID`

---

## ✨ Features

- ✅ CRUD operation testing
- ✅ Status code validation
- ✅ JSON response validation
- ✅ JSON schema validation
- ✅ Dynamic variable handling using Postman variables
- ✅ End-to-end workflow testing
- ✅ Negative testing
- ✅ Newman CLI execution
- ✅ Newman HTML report generation

---

## 🔁 Request Flow

```mermaid
graph TD
    A[GET All Products] --> B[GET Product by Valid ID]
    B --> C[POST Create New Product]
    C --> D[Save Product ID Dynamically]
    D --> E[GET Created Product by Dynamic ID]
    E --> F[PUT Update Created Product]
    F --> G[DELETE Created Product]
    G --> H[Verify Deleted Product]

## 📦 Sample Product Data

```json
{
  "name": "Sugar",
  "price": 90,
  "category": "Grocery"
}
```

## 💻 How to Run

### 1️⃣ Install json-server

```bash
npm install -g json-server
```

### 2️⃣ Run the mock server

```bash
json-server --watch db.json --port 3000
```

### 3️⃣ Import the Postman collection

Import these files into Postman:

- `Product_API_Testing.postman_collection.json`
- `Product_Environment.postman_environment.json`

### 4️⃣ Run tests in Postman Collection Runner

### 5️⃣ Run with Newman CLI

```bash
newman run "Product_API_Testing.postman_collection.json" --env-var "baseURL=http://localhost:3000" -r cli
```

### 6️⃣ Generate Newman HTML Report

```bash
newman run "Product_API_Testing.postman_collection.json" --env-var "baseURL=http://localhost:3000" -r "cli,htmlextra" --reporter-htmlextra-export "newman-report.html"
```

## 📁 Files Included

- `db.json`
- `Product_API_Testing.postman_collection.json`
- `Product_Environment.postman_environment.json`
- `Product API Test Cases.xlsx`
- `newman-report.html`
- `README.md`

## 📸 Screenshots

### 🖥️ Newman CLI Result
<img width="558" height="564" alt="Newman CLI result" src="https://github.com/user-attachments/assets/74589120-5f6d-427b-af20-15df802eab97" />

### 📊 Test Case Report
<img width="960" height="479" alt="Test Case Report" src="https://github.com/user-attachments/assets/be105738-8570-4e57-966c-c9f44810f18e" />

### 🗂️ Collection Structure
<img width="292" height="388" alt="Collection structure" src="https://github.com/user-attachments/assets/c9deff6d-20a1-4fc7-89f3-3d1ab175c836" />

### 📄 Newman HTML Report
<img width="1359" height="682" alt="Newman HTML report" src="https://github.com/user-attachments/assets/99774510-a803-4f46-918e-efe31e060dfc" />

### ✅ Postman Runner All-Pass Result
<img width="1107" height="664" alt="Postman runner all-pass result" src="https://github.com/user-attachments/assets/0aefca27-2bb6-47ce-ac29-30be6447f8fd" />

## 🚀 Future Improvements

- Add authentication-based API testing
- Add more business rule validations
- Add additional modules such as Users or Orders
- Integrate GitHub Actions for automated test execution

## 🔗 Let's Connect with Me

Interested in my work? Feel free to reach out by email or on LinkedIn.

- 📧 [abdullahalmahmudjoy39@gmail.com](mailto:abdullahalmahmudjoy39@gmail.com)
- 💼 [LinkedIn Profile](https://www.linkedin.com/in/abdullah-al-mahmud-joy/)

<p align="center">
  <b>⭐ If you found this project helpful, feel free to give it a star on GitHub!</b>
</p>
