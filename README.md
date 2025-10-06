# 📦 Inventory Management System

A powerful backend-driven application designed to manage and monitor warehouse products efficiently.
Built using **Spring Boot**, **Spring Data JPA**, and **PostgreSQL**, this project provides a complete solution for product inventory management with robust validation and error handling.

---

## 🚀 Features

📦 **Product Management** — Full CRUD (Create, Read, Update, Delete) operations for products
📊 **Stock Tracking** — Manage and update stock levels dynamically
⚠️ **Low Stock Alerts** — Identify products below the defined low-stock threshold
🧩 **Validation & Error Handling** — Handles invalid operations gracefully (e.g., negative stock)
🔗 **RESTful APIs** — Clean, modular API endpoints following REST principles
🛠️ **Database Integration** — Persistent data storage using PostgreSQL
⚡ **Spring Data JPA** — Simplified database interaction with auto-generated queries

---

## 🧠 Tech Stack

| Layer               | Technology         |
| ------------------- | ------------------ |
| **Backend**         | Spring Boot (Java) |
| **ORM**             | Spring Data JPA    |
| **Database**        | PostgreSQL         |
| **Build Tool**      | Maven              |
| **Testing**         | JUnit, Mockito     |
| **Version Control** | Git, GitHub        |
| **Deployment**      | Localhost |

---

## 🎯 **Project Goal**

A backend-heavy API to track products in a warehouse, allowing businesses to maintain product details, update stock efficiently, and monitor low-stock items in real time.

---

## ⚙️ **Core Features**

### **Product Management**

* Full CRUD (Create, Read, Update, Delete) operations for products.
* Each product includes:
  `id`, `name`, `description`, `stockQuantity`, `lowStockThreshold`.

### **Inventory Logic**

* Prevents stock quantity from going below zero.
* Provides dedicated endpoints to:

  * **Increase stock quantity**
  * **Decrease stock quantity** (throws error if insufficient stock)
* Proper error handling for invalid operations (e.g., negative updates).

---

## ✨ **Bonus Features**

🌟 **Low Stock Endpoint**

* Fetch all products currently below their `lowStockThreshold`.

🧪 **Test Cases**

* Unit tests for stock addition/removal logic using **JUnit** and **Mockito**.
* Covers edge cases such as:

  * Trying to remove more stock than available.
  * Invalid input data handling.

---

## 📥 Installation & Setup

Follow these steps to run the project locally 👇

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/krish-0113/Inventory-Management-System-Backend.git
cd Inventory-Management-System-Backend
```

### 2️⃣ Configure Database (PostgreSQL)

Create a database (e.g., `inventory_db`) in PostgreSQL.

Update the `application.properties` file with your credentials:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/inventory_db
spring.datasource.username=postgres
spring.datasource.password=password
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

### 3️⃣ Build and Run Backend

```bash
mvn clean install
mvn spring-boot:run
```

Backend will run on: **[http://localhost:8081](http://localhost:8081)**

---

## 🔗 API Endpoints

| Method   | Endpoint                      | Description                |
| -------- | ----------------------------- | -------------------------- |
| `POST`   | `/api/products`               | Add a new product          |
| `GET`    | `/api/products`               | Get all products           |
| `GET`    | `/api/products/{id}`          | Get product by ID          |
| `PUT`    | `/api/products/{id}`          | Update product             |
| `DELETE` | `/api/products/{id}`          | Delete product             |
| `PUT`    | `/api/products/{id}/increase` | Increase stock             |
| `PUT`    | `/api/products/{id}/decrease` | Decrease stock             |
| `GET`    | `/api/products/low-stock`     | Get all low-stock products |

---

## 🧪 Testing

Run unit tests using:

```bash
mvn test
```



## 💡 Design Choices

✅ Used **Spring Boot** for scalable backend structure
✅ **Spring Data JPA** simplifies database operations
✅ Proper **DTOs and Validation** ensure clean data flow
✅ Chose **PostgreSQL** for reliable relational data management
✅ Emphasized clean REST architecture and modular service design

---
🎥 Demo: Inventory Management API
1. Create Product

Endpoint: POST /products/create
Description: Adds a new product to the inventory with details like name, description, stock quantity, and low stock threshold.
Example Screenshot:
<img width="1906" height="975" alt="Create Product" src="https://github.com/user-attachments/assets/819b6c56-ca79-4308-8652-aeef8be4f18b" />

2. Get All Products

Endpoint: GET /products
Description: Retrieves a list of all products in the inventory.
Example Screenshot:
<img width="1920" height="1080" alt="Get All Products" src="https://github.com/user-attachments/assets/5ed4987e-30c4-43c8-9586-7ba2c888018f" />

3. Get Product by ID

Endpoint: GET /products/{id}
Description: Retrieves details of a specific product using its ID.
Example Screenshot:
<img width="1920" height="1080" alt="Get Product by ID" src="https://github.com/user-attachments/assets/da030ffe-cdd7-4afe-91ac-f5af661a50e5" />

4. Update Product

Endpoint: PUT /products/{id}
Description: Updates details of an existing product.
Example Screenshot:
<img width="1920" height="1080" alt="Update Product" src="https://github.com/user-attachments/assets/c0e11b7a-beab-4f04-95b5-e53daa802695" />

5. Delete Product by ID

Endpoint: DELETE /products/{id}
Description: Removes a product from the inventory using its ID.
Example Screenshot:
<img width="1920" height="1080" alt="Delete Product" src="https://github.com/user-attachments/assets/9f3cc67d-09a7-4602-88e9-3bdcbc362951" />

6. Increase Stock

Endpoint: PATCH /products/{id}/increase-stock
Description: Increases the stock quantity of a specific product.
Example Screenshot:
<img width="1920" height="1080" alt="Increase Stock" src="https://github.com/user-attachments/assets/6d15117c-56de-431e-864c-ac95e062d9f4" />

7. Decrease Stock

Endpoint: PATCH /products/{id}/decrease-stock
Description: Decreases the stock quantity of a specific product.
Example Screenshot:
<img width="1920" height="1080" alt="Decrease Stock" src="https://github.com/user-attachments/assets/e807dbb0-8caa-4b2e-ac85-d2f0ab1b1db4" />

8. Check Low Stock Products

Endpoint: GET /products/low-stock
Description: Lists all products where stock quantity is below the low stock threshold.
Example Screenshot:
<img width="1920" height="1080" alt="Low Stock Products" src="https://github.com/user-attachments/assets/e2a5e4d4-363c-417b-93f8-5d9efeafc8db" />

Note: Duplicate screenshot removed for clarity.
<img width="1920" height="1080" alt="Low Stock Products" src="https://github.com/user-attachments/assets/bdc38ef9-29a5-4d02-94b8-98eacd642a73" />







---

## 👤 Author

**Krishna Jadhav**

* 💼 [LinkedIn Profile](https://www.linkedin.com/in/krishna-jadhav-31760a28a/)
* 💻 [GitHub Profile](https://github.com/krish-0113)

---

## ⭐ Support

If you found this project helpful, please give it a ⭐ on GitHub — it helps a lot!

---

## 📝 License

This project is open source and available under the **MIT License**.

---

**Happy Coding! 🚀**
