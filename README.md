<div align="center">

# 🛒 FreshHut

### Online Grocery Store

A full-stack grocery shopping web application that brings product discovery, cart management, checkout, order tracking, and administration together in one platform.

<p>
  <a href="https://freshhut-grocery.onrender.com/">
    <img src="https://img.shields.io/badge/%F0%9F%9A%80%20LIVE%20WEBSITE-Open%20FreshHut-2e7d32?style=for-the-badge" alt="Live Website">
  </a>
</p>

<img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" alt="HTML5">
<img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" alt="CSS3">
<img src="https://img.shields.io/badge/JavaScript-Vanilla-F7DF1E?style=flat-square&logo=javascript&logoColor=black" alt="JavaScript">
<img src="https://img.shields.io/badge/PHP-8.2-777BB4?style=flat-square&logo=php&logoColor=white" alt="PHP">
<img src="https://img.shields.io/badge/MySQL-Aiven-4479A1?style=flat-square&logo=mysql&logoColor=white" alt="MySQL">
<img src="https://img.shields.io/badge/Docker-Apache-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker">
<img src="https://img.shields.io/badge/Hosted%20on-Render-46E3B7?style=flat-square&logo=render&logoColor=black" alt="Render">

</div>

---

## 📖 About the Project

**FreshHut** is a web-based online grocery store developed as a complete e-commerce style application. Customers can discover grocery products, search by keyword or category, add items to a cart, complete checkout, and follow their order status.

The platform also includes a protected **Admin Panel** for managing products, orders, and users.

The project was developed with **HTML, CSS, JavaScript, PHP, and MySQL**, with the frontend communicating with PHP backend APIs through JSON/Fetch requests.

---

## 📑 Contents

- [About the Project](#-about-the-project)
- [Live Website](#-live-website)
- [Core Features](#-core-features)
- [Screenshots](#-screenshots)
- [Technology Stack](#-technology-stack)
- [How the System Works](#-how-the-system-works)
- [Database](#-database)
- [Project Layout](#-project-layout)
- [Run Locally](#-run-locally)
- [Security](#-security)
- [Demo Accounts](#-demo-accounts)
- [Project Team](#-project-team)
- [License](#-license)

---

<h2 id="-live-website" align="center">🌐 Live Website</h2>

<div align="center">
  <a href="https://freshhut-grocery.onrender.com/">
    <img src="https://img.shields.io/badge/OPEN%20FRESHHUT-Visit%20Live%20Site-2e7d32?style=for-the-badge&logo=render&logoColor=white" alt="Open FreshHut">
  </a>
  <br><br>
  <sub>Hosted on Render. On the free tier, the first request after inactivity may take some time while the service wakes up.</sub>
</div>

---

## ✨ Core Features

### Customer Side

- Account registration and login
- Role-aware access for customers and administrators
- Product browsing by category
- Keyword search and featured products
- Individual product detail pages
- Shopping cart with quantity updates and removal
- Stock validation during cart and checkout operations
- Checkout with:
  - Cash on Delivery
  - bKash
  - Nagad
  - Rocket
- Order confirmation and order history
- Visual order-progress tracking
- Profile editing for name, phone, and delivery address

### Admin Side

- Dashboard with store statistics and recent orders
- Add, edit, and delete products
- Upload product images
- View and update customer orders
- Manage registered users
- Change user roles
- Delete user accounts

---

## 🖼️ Screenshots

<div align="center">

### 🏠 Storefront

<img src="screenshots/homepage.png" alt="FreshHut Homepage" width="850">

### 🔐 Authentication

<table>
<tr>
<td align="center">
<img src="screenshots/register.png" alt="Registration" width="400"><br>
<b>Create Account</b>
</td>
<td align="center">
<img src="screenshots/login.png" alt="Login" width="400"><br>
<b>User Login</b>
</td>
</tr>
</table>

### 🛒 Shopping & Orders

<table>
<tr>
<td align="center">
<img src="screenshots/cart.png" alt="Shopping Cart" width="400"><br>
<b>Shopping Cart</b>
</td>
<td align="center">
<img src="screenshots/order-tracking.png" alt="Order Tracking" width="400"><br>
<b>Order Tracking</b>
</td>
</tr>
</table>

### 🛠️ Administration

<table>
<tr>
<td align="center">
<img src="screenshots/admin-dashboard.png" alt="Admin Dashboard" width="400"><br>
<b>Admin Dashboard</b>
</td>
<td align="center">
<img src="screenshots/admin-manage-products.png" alt="Manage Products" width="400"><br>
<b>Manage Products</b>
</td>
</tr>
</table>

</div>

---

## 🧰 Technology Stack

| Area | Technologies |
|---|---|
| Frontend | HTML5, CSS3, Vanilla JavaScript |
| Backend | PHP 8.2 |
| Database | MySQL |
| API | Fetch API + JSON |
| Server | Apache |
| Container | Docker |
| Database Hosting | Aiven |
| Application Hosting | Render |

### What each layer does

**HTML/CSS** builds the pages and responsive interface.

**JavaScript** handles search, category filtering, cart interactions, checkout requests, UI updates, authentication-side logic, and order tracking.

**PHP** provides the server-side API, authentication, sessions, product operations, cart/order processing, profile operations, and admin authorization.

**MySQL** stores users, categories, products, cart items, orders, and order items.

---

## 🔄 How the System Works

### Customer Journey

```text
Register / Login
      ↓
Browse Products
      ↓
Search or Filter
      ↓
Product Details
      ↓
Add to Cart
      ↓
Checkout
      ├── Delivery Address
      └── Payment Method
      ↓
Place Order
      ↓
Pending
      ↓
Confirmed
      ↓
Processing
      ↓
Out for Delivery
      ↓
Delivered
```

### Admin Journey

```text
Admin Login
    ↓
Admin Dashboard
    ├── Product Management
    ├── Order Management
    └── User Management
```

---

## 🗄️ Database

FreshHut uses a relational MySQL database.

| Table | Main responsibility |
|---|---|
| `users` | Accounts, roles, profile information, and authentication data |
| `categories` | Grocery category definitions |
| `products` | Product information, pricing, stock, description, and images |
| `cart` | Items currently selected by customers |
| `orders` | Order address, payment method, total, and status |
| `order_items` | Product-level details belonging to each order |

Relationships between the cart and order tables are maintained using foreign keys.

---

## 📁 Project Layout

```text
Grocery-Store1/
├── admin/
│   ├── index.html
│   ├── products.html
│   ├── orders.html
│   ├── users.html
│   └── admin-style.css
├── api/
│   ├── auth_check.php
│   ├── cart.php
│   ├── login.php
│   ├── logout.php
│   ├── orders.php
│   ├── products.php
│   ├── register.php
│   ├── user.php
│   └── users.php
├── user/
├── config/
│   ├── db.php
│   ├── ca.pem
│   └── grocery_store.sql
├── css/
├── js/
├── uploads/
├── about.html
├── cart.html
├── checkout.html
├── contact.html
├── index.html
├── login.html
├── product-detail.html
├── products.html
├── register.html
├── tracking.html
├── Dockerfile
└── entrypoint.sh
```

---

## 💻 Run Locally

### Requirements

- XAMPP with Apache and MySQL
- Git
- A modern web browser

### Setup

1. Clone the repository into the XAMPP `htdocs` directory.

```bash
cd C:/xampp/htdocs
git clone <your-repository-url>
cd Grocery-Store1
```

2. Start **Apache** and **MySQL** from XAMPP.

3. Create a local database through phpMyAdmin, for example:

```text
grocery_store
```

4. Configure the local database settings in `config/db.php`.

Typical XAMPP values are:

```php
DB_HOST = "localhost";
DB_USER = "root";
DB_PASS = "";
DB_NAME = "grocery_store";
DB_PORT = 3306;
```

5. Open the application in your browser through your local Apache URL.

---

## 🔐 Security

The project includes several application-level protections:

- Password hashing for stored passwords
- PHP session-based authentication
- Role-based authorization for admin functions
- Session validation for protected pages
- Users restricted to viewing their own orders
- Stock checks before completing orders
- Prepared database statements
- Database transactions for checkout and stock updates
- SSL support for the hosted MySQL connection

---

## 👤 Demo Accounts

The current seeded demo provides separate customer and administrator accounts.

| Role | Email | Password |
|---|---|---|
| Admin | `admin@freshhut.com` | `FreshHut_Admin_2026!` |
| Customer | `customer@test.com` | `customer123` |

> These credentials are intended for testing the project. Avoid using them as real production credentials.

---

## 🤝 Contributing

Have ideas or improvements? Feel free to fork the repository, apply your changes, and submit a pull request.

---

## 🔐 License

This project is licensed under the [MIT License](./LICENSE).

---

## ✉️ Contact

For any questions or concerns, feel free to reach out by email at abdullahasan220618@gmail.com
