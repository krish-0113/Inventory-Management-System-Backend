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
| **Deployment**      | Render / Localhost |

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
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

### 3️⃣ Build and Run Backend

```bash
mvn clean install
mvn spring-boot:run
```

Backend will run on: **[http://localhost:8080](http://localhost:8080)**

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

### Example Test JSON

```json
{
  "name": "Laptop 4",
  "description": "HP Pavilion 17",
  "stockQuantity": 20,
  "lowStockThreshold": 3
}
```

---

## 💡 Design Choices

✅ Used **Spring Boot** for scalable backend structure
✅ **Spring Data JPA** simplifies database operations
✅ Proper **DTOs and Validation** ensure clean data flow
✅ Chose **PostgreSQL** for reliable relational data management
✅ Emphasized clean REST architecture and modular service design

---

## 🎥 Demo

🔗 **Video Demo Link:** 

---

## 👤 Author

**Krishna Jadhav**

* 💼 [LinkedIn Profile](https://www.linkedin.com/in/krishna-jadhav)
* 💻 [GitHub Profile](https://github.com/krish-0113)

---

## ⭐ Support

If you found this project helpful, please give it a ⭐ on GitHub — it helps a lot!

---

## 📝 License

This project is open source and available under the **MIT License**.

---

**Happy Coding! 🚀**
