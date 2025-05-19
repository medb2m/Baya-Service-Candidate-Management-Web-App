# 📱 Baya Service – Candidate Management Web App

**Baya Service** is a lightweight PHP + MySQL application for managing candidate phone numbers and offers. Built for a freelance client, it’s optimized for mobile use, Arabic/English localization, and non-technical users.

---

## ✨ Features

- 📲 Add candidate information (name, phone, offer)
- 🔐 PIN-protected access to candidate list
- 🌐 Arabic 🇸🇦 and English 🇬🇧 language support with RTL layout
- 📱 Fully responsive and mobile-friendly
- ✅ Works on shared hosting (Hostinger) or locally via XAMPP/WAMP

---

## 🖥️ Screenshots

![screenshot](docs/screenshot-form.png)  
![screenshot](docs/screenshot-list.png)

---

## 🗂 Tech Stack

- PHP 8+
- MySQL
- HTML5/CSS3
- Font Awesome
- AOS (Animate on Scroll)
- No external framework (fully lightweight)

---

## 🔐 Access

- The candidate list is protected by a 4-digit PIN
- **Default PIN**: `1234` (you can change it in `list.php`)

---

## 🧪 Local Setup (XAMPP / WAMP)

### ✅ Prerequisites

- PHP 7.4+ (or 8.x)
- MySQL
- Apache (via XAMPP or WAMP)

### 🛠️ Steps

1. **Clone or download** the repository

```bash
git clone https://github.com/your-username/baya-service.git
```

2. **Place the folder** into your server root:
   - For **XAMPP**: `C:/xampp/htdocs/baya-service`
   - For **WAMP**: `C:/wamp64/www/baya-service`

3. **Create the database**:

- Open [phpMyAdmin](http://localhost/phpmyadmin)
- Create a new database (e.g., `baya_service`)
- Run this SQL to create the table:

```sql
CREATE TABLE candidates (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    phone VARCHAR(20) NOT NULL,
    offer VARCHAR(255) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

4. **Configure DB credentials**  
   Edit `db.php`:

```php
$host = "localhost";
$db = "baya_service";     // Your database name
$user = "root";           // Default for XAMPP/WAMP
$pass = "";               // Leave empty if no password
```

5. ✅ Access the app at:  
   - [http://localhost/baya-service/add.php](http://localhost/baya-service/add.php)
   - [http://localhost/baya-service/list.php](http://localhost/baya-service/list.php)

---

## 📁 Folder Structure

```
/baya-service
├── add.php
├── list.php
├── index.php
├── db.php
├── assets/
│   ├── style.css
│   └── logo_baya.png
├── insert_candidates.sql
└── README.md
```

---

## 🌍 Hosting

This app is already hosted using [Hostinger Shared Hosting](https://hostinger.com) using PHP/MySQL with File Manager deployment.

---

## 📄 License

This project was developed as a private freelance solution. Feel free to fork, customize, or build on top of it.

---

## ✉️ Contact

For questions or custom freelance work:  
📧 your.email@example.com
