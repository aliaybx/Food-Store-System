# Freshcery - Organic Grocery E-Commerce Store

[![PHP Version](https://img.shields.io/badge/PHP-7.4+-777BB4?style=flat&logo=php)](https://www.php.net/)
[![MySQL](https://img.shields.io/badge/MySQL-10.4+-00758F?style=flat&logo=mysql)](https://www.mysql.com/)
[![Bootstrap](https://img.shields.io/badge/Bootstrap-4.x-7952B3?style=flat&logo=bootstrap)](https://getbootstrap.com/)
[![License](https://img.shields.io/badge/License-MIT-FF5722?style=flat)](LICENSE)
[![Stars](https://img.shields.io/github/stars/aliaybx/Food-Store-System?style=flat)](https://github.com/aliaybx/Food-Store-System/stargazers)
[![Issues](https://img.shields.io/github/issues/aliaybx/Food-Store-System?style=flat)](https://github.com/aliaybx/Food-Store-System/issues)

> A production-ready organic groceries e-commerce platform built with PHP, MySQL, and Bootstrap. Freshcery brings farm-to-table freshness directly to customers' doors.

## 📋 Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Security](#security)
- [Database Schema](#database-schema)
- [Contributing](#contributing)
- [License](#license)
- [Screenshots](#screenshots)

## ✨ Features

### Customer Features
- 🛒 **Shopping Cart** - Add, update, and remove products seamlessly
- 👤 **User Authentication** - Secure registration and login system
- 📦 **Order Management** - Place orders and track history
- 🔍 **Product Browsing** - Browse by categories (Vegetables, Meats, Fish, Fruits)
- 🏠 **User Dashboard** - Manage profile and view transaction history

### Admin Features
- 📊 **Dashboard** - Overview of products, orders, categories, and admins
- 🏷️ **Product Management** - Create, read, update, delete products
- 📁 **Category Management** - Organize products into categories
- 📋 **Order Management** - View and update order status
- 👥 **Admin Management** - Manage admin accounts

## 🛠 Tech Stack

| Category | Technology |
|----------|------------|
| **Backend** | PHP 7.4+ (PDO) |
| **Database** | MySQL / MariaDB |
| **Frontend** | HTML5, CSS3, JavaScript |
| **CSS Framework** | Bootstrap 4 |
| **JavaScript** | jQuery |
| **Icons** | Font Awesome, SB Bistro Icons |

## 🚀 Installation

### Prerequisites
- PHP 7.4 or higher
- MySQL 5.7+ or MariaDB 10.4+
- Apache/Nginx web server
- Composer (optional, for dependencies)

### Step 1: Clone the Repository

```bash
git clone https://github.com/aliaybx/Food-Store-System.git
cd Food-Store-System
```

### Step 2: Configure Database

1. Create a new MySQL database:
```sql
CREATE DATABASE freshcery CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
```

2. Import the database schema:
```bash
mysql -u root -p freshcery < freshcery.sql
```

### Step 3: Configure Application

Edit `config/config.php` with your database credentials:

```php
define("HOST", "localhost");
define("DBNAME", "freshcery");
define("USER", "your_username");
define("PASS", "your_password");
```

### Step 4: Configure Web Server

**For Apache (XAMPP/WAMP):**
- Place the project in `htdocs` folder
- Access via: `http://localhost/freshcery`

**For Apache (Virtual Host):**
```apache
<VirtualHost *:80>
    ServerName freshcery.local
    DocumentRoot "C:/path/to/Freshcery"
    <Directory "C:/path/to/Freshcery">
        Options -Indexes +FollowSymLinks
        AllowOverride All
        Require all granted
    </Directory>
</VirtualHost>
```

### Step 5: Default Admin Credentials

```
Email: admin.first@gmail.com
Password: 123456
```

## 📁 Project Structure

```
Freshcery/
├── admin-panel/           # Admin dashboard
│   ├── ADMINS/           # Admin authentication
│   ├── categories-admins/ # Category management
│   ├── orders-admins/    # Order management
│   ├── products-admins/  # Product management
│   ├── LAYOUTS/          # Admin layouts
│   └── STYLES/           # Admin styles
├── assets/               # Static assets
│   ├── CSS/              # Custom styles
│   ├── FONTS/            # Icon fonts
│   ├── IMG/              # Images
│   ├── JS/               # JavaScript files
│   ├── MEDIA/            # Media files
│   ├── PACKAGES/         # Third-party libraries
│   └── SASS/             # SASS files
├── AUTH/                 # User authentication
├── CONFIG/               # Configuration files
├── INCLUDES/             # Shared includes (header/footer)
├── PRODUCTS/              # Product-related pages
├── SQL_FILE/             # SQL database file
├── USERS/                # User dashboard
├── 404.php               # 404 error page
├── ABOUT.php             # About page
├── CONTACT.php           # Contact page
├── FAQ.php               # FAQ page
├── INDEX.php             # Home page
├── SHOP.php              # Shop page
└── freshcery.sql         # Database schema
```

## 🔒 Security

### Implemented Security Measures
- ✅ **Password Hashing** - Using PHP's `password_hash()` with bcrypt
- ✅ **PDO Prepared Statements** - Prevents SQL injection attacks
- ✅ **Session Management** - Secure session handling
- ✅ **Input Sanitization** - XSS prevention
- ✅ **File Upload Validation** - Secure image uploads

### Recommended Security Improvements
- Add CSRF tokens to all forms
- Implement rate limiting for login attempts
- Add two-factor authentication
- Use HTTPS in production
- Implement proper error logging
- Add input validation libraries

## 🗄️ Database Schema

### Tables Overview

| Table | Description |
|-------|-------------|
| `users` | Registered customers |
| `admins` | Admin accounts |
| `categories` | Product categories |
| `products` | Product inventory |
| `cart` | Shopping cart items |
| `orders` | Customer orders |

### Key Relationships
- Users → Orders (One-to-Many)
- Categories → Products (One-to-Many)
- Users → Cart (One-to-Many)

## 🤝 Contributing

Contributions are welcome! Please read our [contributing guidelines](CONTRIBUTING.md) first.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📸 Screenshots

### Customer Interface
- **Home Page** - Hero section with video background
- **Shop** - Product grid with category filtering
- **Cart** - Shopping cart with quantity controls
- **Checkout** - Order form with validation

### Admin Dashboard
- **Dashboard** - Statistics overview
- **Products** - CRUD operations
- **Orders** - Order management
- **Categories** - Category management

---

<p align="center">
  Made with ❤️ by <a href="https://github.com/aliaybx">Ali Ayoub</a>
</p>

<p align="center">
  <a href="https://github.com/aliaybx/Food-Store-System">
    <img src="https://img.shields.io/github/forks/aliaybx/Food-Store-System?style=social" alt="Forks">
  </a>
  <a href="https://github.com/aliaybx/Food-Store-System">
    <img src="https://img.shields.io/github/stars/aliaybx/Food-Store-System?style=social" alt="Stars">
  </a>
</p>
