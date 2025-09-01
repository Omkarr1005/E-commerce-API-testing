🛒 E-commerce API Testing with Postman & Newman
📌 Project Overview
This project demonstrates API testing of a sample E-commerce platform using Postman.
The test collection covers the end-to-end customer journey including:

User login & token generation

Viewing products

Fetching product details

Adding items to the cart

Updating the cart

Automation is achieved using Postman Tests and Newman for command-line execution and reporting.

⚙️ Tech Stack
Postman – API request building & test automation

JavaScript (pm scripts) – Writing test validations

Newman – CLI-based test runner for Postman

Node.js – Required for Newman

🛠️ Features Tested
Login (POST /auth/login)

Validate successful login

Capture and store Bearer Token

Get All Products (GET /products)

Validate response status = 200

Ensure product list is not empty

Get Product by ID (GET /products/1)

Validate product has title field

Add to Cart (POST /carts)

Create a new cart with product(s)

Verify cart creation success

Update Cart (PUT /carts/{id})

Update product quantity in cart

Validate updated response

🔄 Request Chaining
Token from Login is stored in {{token}} variable

cartId captured from Add to Cart response → used in Update Cart

This makes the test flow dynamic & realistic.


Project structure 
📁 Ecommerce-API-Testing
 ┣ 📄 EcommerceAPI.postman_collection.json
 ┣ 📄 EcommerceEnv.postman_environment.json
 ┣ 📄 README.md

