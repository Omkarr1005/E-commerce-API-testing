# 🛒 E-commerce API Testing Project (Postman & Newman)

## 📌 Project Overview
This project involves **API testing** of an **E-commerce application** using **Postman** and **Newman**.  
Automation was implemented for key workflows including login, product retrieval, cart management, and dynamic request chaining using tokens.

## 🎯 Objectives
- Automate API testing of E-commerce workflows.  
- Validate responses, status codes, and data integrity.  
- Implement dynamic, realistic test flows using token-based authentication.  
- Generate automated reports using Newman.

## ⚙️ Tech Stack
- **Postman** – API request building & test automation  
- **JavaScript (pm scripts)** – Writing test validations  
- **Newman** – CLI-based test runner for Postman collections  
- **Node.js** – Required for Newman execution  

## ✅ Features Tested
1. **User Login (POST /auth/login)**  
   - Validate successful login  
   - Capture and store Bearer Token for subsequent requests  

2. **Get All Products (GET /products)**  
   - Validate response status = 200  
   - Ensure product list is not empty  

3. **Get Product by ID (GET /products/1)**  
   - Validate product has a title field  

4. **Add to Cart (POST /carts)**  
   - Create a new cart with product(s)  
   - Verify cart creation success  
   - Capture `cartId` for further requests  

5. **Update Cart (PUT /carts/{id})**  
   - Update product quantity in cart  
   - Validate updated response  

## 🔄 Request Chaining
- **Token Handling:** Token from login is stored in `{{token}}` variable.  
- **Dynamic Cart Handling:** `cartId` captured from Add to Cart response → used in Update Cart request.  
- Enables realistic workflow simulation across multiple API calls.

## 📝 Sample Test Validations
| Endpoint             | Validation Description |
|---------------------|----------------------|
| POST /auth/login     | Response contains Bearer Token; status = 200 |
| GET /products        | Status = 200; product list not empty |
| GET /products/1      | Product object contains `title` field |
| POST /carts          | Cart created successfully; response contains `cartId` |
| PUT /carts/{id}      | Updated cart quantity reflected in response |

## 🚀 Outcome
- Automated E-commerce API workflows with dynamic data and token handling.  
- Ensured correctness of critical endpoints (login, product retrieval, cart operations).  
- Reduced manual effort using Postman tests + Newman CLI execution.  
- Delivered structured execution reports for validation and stakeholder review.

---
👨‍💻 **Tester/Automation Engineer:** Omkar Sanas  
📅 **Duration:** Internship / Personal Project  
🛠️ **Role:** API Testing Engineer (Postman & Newman)  
