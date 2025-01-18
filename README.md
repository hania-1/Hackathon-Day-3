# E-Commerce Marketplace - Product Management with Sanity CMS

## 📌 Project Overview  
The **E-Commerce Marketplace** integrates **Sanity CMS** with a custom API to manage products in a seamless manner. It allows for product CRUD operations, fetching product data from Sanity CMS, and displaying it within a Next.js application.

---

## 🌟 Features  
- **Fetch All Products**: Retrieve a list of all products stored in Sanity CMS.
- **Fetch Single Product**: Get details of a specific product by its unique ID.
- **Create Product**: Add new products to the CMS with fields like title, price, description, image, and more.
- **Update Product**: Modify details of an existing product by its ID.
- **Responsive Layout**: Display products in a responsive grid layout.

---

## 🏗️ System Architecture  

### Frontend  
- Built with **Next.js** to render pages and fetch data from APIs.

### CMS  
- **Sanity CMS** is used to manage product data.

### API Endpoints  
- **Products API**: Interacts with **Sanity CMS** to fetch, create, and update product data.

### Architecture Diagram  
```css
[Frontend (Next.js)]
    |
[Sanity CMS] --> [Product Data API]
🛠️ Technical Requirements
Frontend
Next.js for building the user interface.
React for dynamic rendering.
Tailwind CSS for styling.
CMS
Sanity CMS to manage products.
API Endpoints
1️⃣ GET /api/products: Fetches all products from Sanity CMS. 2️⃣ GET /api/products/:id: Fetches a specific product by ID. 3️⃣ POST /api/products: Creates a new product in Sanity CMS. 4️⃣ PUT /api/products/:id: Updates an existing product by ID.

📡 API Endpoints
1️⃣ GET /api/products
Fetches a list of all products from Sanity CMS.

Example Response:

json
Copy
Edit
[
  {
    "id": "1",
    "name": "Product A",
    "price": 100,
    "description": "A great product."
  }
]
2️⃣ GET /api/products/:id
Fetches details of a single product by its unique ID.

Example Response:

json
Copy
Edit
{
  "id": "1",
  "name": "Product A",
  "price": 100,
  "description": "A great product.",
  "image": "url_to_image",
  "category": "Electronics"
}
3️⃣ POST /api/products
Creates a new product in Sanity CMS.

Example Request Body:

json
Copy
Edit
{
  "name": "Product A",
  "price": 100,
  "description": "A great product.",
  "image": "url_to_image",
  "category": "Electronics"
}
4️⃣ PUT /api/products/:id
Updates an existing product by its ID.

Example Request Body:

json
Copy
Edit
{
  "name": "Updated Product",
  "price": 120,
  "description": "An updated description.",
  "image": "url_to_updated_image",
  "category": "Electronics"
}
📝 Sanity Schema Documentation
1️⃣ Product Schema
Defines the structure of the product document in Sanity CMS.

javascript
Copy
Edit
export default {
  name: "product",
  type: "document",
  title: "Product",
  fields: [
    { name: "name", type: "string", title: "Product Name" },
    { name: "price", type: "number", title: "Price" },
    { name: "description", type: "text", title: "Description" },
    { name: "image", type: "image", title: "Product Image" },
    { name: "category", type: "string", title: "Category" }
  ]
};
