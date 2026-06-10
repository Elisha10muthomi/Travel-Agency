# 🌟 Luxe Voyage - Travel Agency & Luxury Hotel Booking System

[![PHP](https://img.shields.io/badge/PHP-7.4+-777BB4.svg)](https://php.net/)
[![MySQL](https://img.shields.io/badge/MySQL-5.7+-4479A1.svg)](https://mysql.com/)
[![XAMPP](https://img.shields.io/badge/XAMPP-Compatible-FB7A24.svg)](https://apachefriends.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

A premium hotel booking platform with three user roles: **Admin**, **Host**, and **Customer**. Built with PHP and MySQL for seamless luxury travel experiences.

## ✨ Features

### 👑 Admin Features
- Full system oversight and analytics
- User management (approve hosts, manage customers)
- Destination and hotel verification
- Booking monitoring and reporting
- Revenue tracking and platform statistics

### 🏨 Host Features
- Hotel/property registration and management
- Room inventory management
- Booking confirmation and cancellation
- Revenue dashboard and analytics
- Profile management and document submission

### 👤 Customer Features
- Browse luxury hotels and destinations
- Search and filter accommodations
- Real-time booking and payment
- Booking history and management
- Review and rating system
- Wishlist creation

## 🚀 Quick Installation Guide

### Prerequisites
- **XAMPP** (or any local PHP/MySQL environment)
- **Web Browser** (Chrome, Firefox, Edge)
- **Text Editor** (VS Code, Sublime Text, etc.)

### Step 1: Install XAMPP

1. Download XAMPP from [Apache Friends](https://www.apachefriends.org/)
2. Install on your Windows/Linux/Mac system
3. Open **XAMPP Control Panel**
4. Start both services:
   - Click **Start** for **Apache**
   - Click **Start** for **MySQL**

### Step 2: Set Up the Project



**Or download the ZIP file** and extract it.

**Move to htdocs:**
- Copy the `Luxe-Voyage` folder to XAMPP's `htdocs` directory:
  - Windows: `C:\xampp\htdocs\`
  - Mac: `/Applications/XAMPP/htdocs/`
  - Linux: `/opt/lampp/htdocs/`

### Step 3: Import Database

#### Method A: phpMyAdmin (Recommended)

1. Open browser and navigate to: `http://localhost/phpmyadmin`
2. Click **"New"** in left sidebar
3. Enter database name: `luxe_voyage`
4. Select **utf8mb4_general_ci** as collation
5. Click **"Create"**
6. Click **"Import"** tab
7. Click **"Choose File"** and select `database.sql` from the project folder
8. Click **"Go"** at the bottom

#### Method B: Command Line

**Windows:**
```cmd
cd C:\xampp\mysql\bin
mysql -u root -p < "C:\xampp\htdocs\Luxe-Voyage\database.sql"
```

**Mac/Linux:**
```bash
cd /Applications/XAMPP/bin
./mysql -u root -p < /Applications/XAMPP/htdocs/Luxe-Voyage/database.sql
```

### Step 4: Configure Database Connection

Open `config/database.php` and update credentials if needed:

```php
define('DB_HOST', 'localhost');
define('DB_USER', 'root');
define('DB_PASS', '');  // Set your MySQL password
define('DB_NAME', 'luxe_voyage');
```

### Step 5: Create Required Directories

**Windows (Command Prompt):**
```cmd
cd C:\xampp\htdocs\Luxe-Voyage
mkdir uploads
mkdir uploads\destinations
mkdir uploads\hotels
mkdir uploads\profiles
```

**Mac/Linux (Terminal):**
```bash
cd /Applications/XAMPP/htdocs/Luxe-Voyage
mkdir -p uploads/destinations uploads/hotels uploads/profiles
```

### Step 6: Set File Permissions

**Windows:** Usually automatic; no action needed

**Mac/Linux:**
```bash
chmod -R 755 uploads/
```

## 🎯 Running the Application

1. Ensure **Apache** and **MySQL** are running in XAMPP Control Panel
2. Open your web browser
3. Navigate to: `http://localhost/Luxe-Voyage/index.php`
4. You're ready to go! 🎉

## 🔑 Default Login Credentials

| Role | Email | Password |
|------|-------|----------|
| **Admin** | admin@luxevoyage.com | admin123 |
| **Host** | host@luxevoyage.com | host123 |
| **Customer** | customer@luxevoyage.com | customer123 |

*Note: Register new accounts through the signup page.*

## 📁 Project Structure

```
Luxe-Voyage/
├── index.php                 # Landing page
├── admin/                    # Admin dashboard
│   ├── dashboard.php
│   ├── users.php
│   ├── bookings.php
│   └── reports.php
├── host/                     # Host dashboard
│   ├── dashboard.php
│   ├── hotels.php
│   ├── rooms.php
│   └── bookings.php
├── customer/                 # Customer dashboard
│   ├── dashboard.php
│   ├── bookings.php
│   ├── wishlist.php
│   └── profile.php
├── assets/                   # Static assets
│   ├── css/
│   ├── js/
│   ├── images/
│   └── fonts/
├── uploads/                  # User uploaded files
│   ├── destinations/
│   ├── hotels/
│   └── profiles/
├── config/                   # Configuration files
│   └── database.php
├── includes/                 # Reusable components
│   ├── header.php
│   ├── footer.php
│   └── functions.php
└── database.sql              # Database structure and sample data
```

## 🛠️ Technology Stack

| Technology | Purpose |
|------------|---------|
| **PHP** (7.4+) | Backend logic |
| **MySQL** | Database management |
| **HTML5/CSS3** | Frontend structure & styling |
| **JavaScript** | Interactive features |
| **Bootstrap 5** | Responsive design |
| **jQuery** | DOM manipulation |
| **AJAX** | Asynchronous requests |

## 📱 Responsive Design

- Fully responsive across all devices
- Mobile-first approach
- Optimized for tablet and desktop views
- Touch-friendly interface

## 🔒 Security Features

- Password hashing (bcrypt)
- SQL injection prevention (PDO/prepared statements)
- XSS protection
- CSRF tokens
- Session management
- Input validation and sanitization

## 🐛 Troubleshooting

### Common Issues & Solutions

**Issue:** "Access denied for user 'root'@'localhost'"
- **Solution:** Check MySQL credentials in `config/database.php`

**Issue:** "500 Internal Server Error"
- **Solution:** Check file permissions and .htaccess configuration

**Issue:** Database connection failed
- **Solution:** Ensure MySQL is running in XAMPP Control Panel

**Issue:** Upload directory not writable
- **Solution:** Run the mkdir commands above to create directories

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Development Guidelines
- Follow PSR coding standards
- Comment your code where necessary
- Update documentation for new features
- Test thoroughly before submitting

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


## 📞 Support

For support inquiries:
- 📧 Email: support@luxevoyage.com
- 🌐 Website: https://luxevoyage.com
- 📱 Phone: +1 (555) 123-4567

## 🙏 Acknowledgments

- Bootstrap team for the amazing framework
- Font Awesome for icons
- Unsplash for stock images
- All beta testers and contributors

---

**Made with ❤️ for luxury travelers worldwide**


