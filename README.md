# Pharmacy-Management-System
Pharmacy Management System
# Pharmacy Management System | سیستەمی بەڕێوەبردنی دەرمانخانە

A PHP/MySQL pharmacy management system designed for local pharmacy inventory, POS sales, purchases, prescriptions, stock control, reports, and backup support.
سیستەمی بەڕێوەبردنی دەرمانخانە بە PHP و MySQL کە بۆ بەڕێوەبردنی دەرمان، فرۆشتن، کڕین، وەسفە، کۆگا، ڕاپۆرت و backup دروستکراوە.

---

## English

## Overview

This project is a pharmacy management system built with **PHP**, **MySQL/MariaDB**, **HTML**, **CSS**, and **JavaScript**. It is designed to run locally using XAMPP or on a local server/mini PC for pharmacy use.

The system supports medicine inventory, batches, expiry tracking, POS sales, purchases, suppliers, prescriptions, user roles, audit logs, reports, and backup scripts.

> Important: This project is suitable for learning, demo, and controlled testing. Before using it in a real pharmacy, it should be tested carefully, reviewed for security, and checked against local pharmacy/legal requirements.

---

## Features

* Admin login system
* Dashboard with pharmacy statistics
* Medicine management
* Medicine batches and expiry dates
* Low-stock alerts
* Near-expiry and expired-stock tracking
* Supplier management
* Purchase management
* POS sales system
* Sales receipts
* Prescription management
* Pharmacist approval workflow
* User roles and permissions
* Stock adjustment system
* Audit logs
* Reports
* CSV medicine import
* Database backup scripts
* Kurdish Sorani RTL interface support
* Responsive UI improvements
* Sidebar scrolling fix for laptop screens

---

## User Roles

| Role       | Permissions                              |
| ---------- | ---------------------------------------- |
| Admin      | Full system access                       |
| Manager    | Inventory, purchases, reports, suppliers |
| Pharmacist | Sales, prescriptions, medicine checks    |
| Cashier    | POS sales only                           |

---

## Technologies Used

* PHP 8+
* MySQL / MariaDB
* HTML5
* CSS3
* JavaScript
* XAMPP / Apache
* phpMyAdmin

---

## Installation Using XAMPP

### 1. Download or clone the project

```bash
git clone https://github.com/your-username/pharmacy-management-system.git
```

Or download the ZIP file and extract it.

### 2. Move the project to XAMPP htdocs

On Windows:

```text
C:\xampp\htdocs\pharmacy_xampp_redesigned
```

On macOS XAMPP:

```text
/Applications/XAMPP/xamppfiles/htdocs/pharmacy_xampp_redesigned
```

### 3. Start XAMPP

Start:

```text
Apache
MySQL
```

### 4. Import the database

Open phpMyAdmin:

```text
http://localhost/phpmyadmin
```

Import:

```text
sql/pharmacy_db.sql
```

The database name should be:

```text
pharmacy_db
```

### 5. Configure database connection

Check:

```text
config/db.php
```

Default local XAMPP settings:

```php
$host = 'localhost';
$user = 'root';
$pass = '';
$dbname = 'pharmacy_db';
```

For real use, do not use an empty database password.

### 6. Open the system

```text
http://localhost/pharmacy_xampp_redesigned/
```

---

## Default Demo Login

```text
Email: admin@pharmacy.local
Password: admin123
```

Change the password immediately after login.

---

## CSV Medicine Import Format

The required CSV column is:

```text
name
```

Optional columns:

```text
generic_name, barcode, category, min_stock, quantity, expiry_date, purchase_price, selling_price, batch_number, supplier
```

Example header:

```csv
name,generic_name,barcode,category,min_stock,quantity,expiry_date,purchase_price,selling_price,batch_number,supplier
```

---

## Backup

A macOS XAMPP backup script is included:

```text
scripts/backup_database_mac_xampp.sh
```

Run it manually:

```bash
/Applications/XAMPP/xamppfiles/htdocs/pharmacy_xampp_redesigned/scripts/backup_database_mac_xampp.sh
```

Backups are saved to:

```text
/Users/Shared/pharmacy_backups
```

For real pharmacy use, backups should also be copied to an external drive or secure cloud storage.

---

## Recommended Real-Life Setup

For a real pharmacy, it is better to run the system on a dedicated local server or mini PC.

Recommended setup:

```text
Mini PC / local server
Apache or Nginx
PHP
MariaDB
Automatic database backup
UPS power backup
Desktop browser shortcut
Barcode scanner
Receipt printer
```

Users should open the system from a shortcut such as:

```text
http://192.168.1.10/pharmacy/
```

This avoids manually opening XAMPP every time.

---

## Security Notes

Before real-life use, make sure to:

* Change default admin password
* Use strong database credentials
* Enable HTTPS if accessed over a network or internet
* Keep backups outside the main computer
* Test database restore
* Review user permissions
* Review file upload security
* Review CSRF protection
* Review audit logs
* Disable public debug output
* Do not upload `.env`, backups, or database dumps to GitHub

Recommended `.gitignore` entries:

```gitignore
.env
storage/backups/
*.sql
*.zip
```

---

## Production Readiness Warning

This project should not be considered fully production-ready without:

* Full security audit
* Pharmacy workflow review by a pharmacist
* Local legal/regulatory review
* Backup and restore testing
* Barcode scanner testing
* Receipt printer testing
* Multi-user testing
* Server hardening

---

## Suggested Screenshots

Add screenshots here:

```text
screenshots/login.png
screenshots/dashboard.png
screenshots/medicines.png
screenshots/pos.png
screenshots/reports.png
```

Example:

```markdown
![Dashboard](screenshots/dashboard.png)
```

---

## Roadmap

Planned improvements:

* Full installer for Windows
* Better non-XAMPP deployment
* Cloud backup integration
* HTTPS local server guide
* Expense management
* Net profit/loss report
* Barcode label printing
* Advanced prescription safety checks
* Multi-branch pharmacy support
* Mobile-friendly POS mode

---

## License

This project is for educational and demonstration purposes.
Add your preferred license here, for example:

```text
MIT License
```

---

# کوردی

## پێناسەی پڕۆژە

ئەم پڕۆژەیە سیستەمی بەڕێوەبردنی دەرمانخانەیە کە بە **PHP** و **MySQL/MariaDB** دروستکراوە. دەتوانرێت لەسەر XAMPP یان server/mini PC ـی ناوخۆیی بەکاربهێنرێت.

سیستەمەکە پشتگیری دەکات لە بەڕێوەبردنی دەرمان، batch، بەسەرچوون، فرۆشتن، کڕین، دابینکەر، وەسفە، role ـی بەکارهێنەر، audit log، ڕاپۆرت و backup.

> گرنگ: ئەم پڕۆژەیە باشە بۆ فێربوون، demo و تاقیکردنەوە. پێش بەکارهێنانی لە دەرمانخانەی ڕاستەقینە، پێویستە بە وردی تاقی بکرێتەوە، security review بکرێت و یاسا و ڕێنمایی ناوخۆیی چێک بکرێت.

---

## تایبەتمەندییەکان

* سیستەمی login بۆ admin
* dashboard بۆ ئامارەکانی دەرمانخانە
* بەڕێوەبردنی دەرمان
* batch و بەرواری بەسەرچوون
* ئاگادارکردنەوەی stock ـی کەم
* ئاگادارکردنەوەی دەرمانی نزیک بە بەسەرچوون
* بەڕێوەبردنی دابینکەر
* بەڕێوەبردنی کڕین
* سیستەمی POS بۆ فرۆشتن
* receipt بۆ فرۆشتن
* بەڕێوەبردنی وەسفە
* approve ـی دەرمانساز بۆ وەسفە
* role و permission ـی بەکارهێنەر
* stock adjustment
* audit logs
* ڕاپۆرتەکان
* import ـی دەرمان بە CSV
* script ـی backup
* پشتگیری زمانی کوردی سۆرانی و RTL
* UI ـی responsive
* چاککردنی scroll ـی sidebar بۆ laptop

---

## ڕۆڵەکانی بەکارهێنەر

| ڕۆڵ        | دەسەڵات                      |
| ---------- | ---------------------------- |
| Admin      | دەسەڵاتی تەواو               |
| Manager    | کۆگا، کڕین، ڕاپۆرت، دابینکەر |
| Pharmacist | فرۆشتن، وەسفە، چێکی دەرمان   |
| Cashier    | تەنها POS و فرۆشتن           |

---

## تەکنەلۆجیای بەکارهاتوو

* PHP 8+
* MySQL / MariaDB
* HTML5
* CSS3
* JavaScript
* XAMPP / Apache
* phpMyAdmin

---

## دامەزراندن بە XAMPP

### 1. پڕۆژەکە دابگرە یان clone بکە

```bash
git clone https://github.com/your-username/pharmacy-management-system.git
```

یان ZIP ـەکە دابگرە و extract ـی بکە.

### 2. پڕۆژەکە بخە ناو htdocs

لە Windows:

```text
C:\xampp\htdocs\pharmacy_xampp_redesigned
```

لە macOS XAMPP:

```text
/Applications/XAMPP/xamppfiles/htdocs/pharmacy_xampp_redesigned
```

### 3. XAMPP بکەرەوە

ئەم دووانە start بکە:

```text
Apache
MySQL
```

### 4. Database import بکە

phpMyAdmin بکەرەوە:

```text
http://localhost/phpmyadmin
```

ئەم فایلە import بکە:

```text
sql/pharmacy_db.sql
```

ناوی database دەبێت:

```text
pharmacy_db
```

### 5. ڕێکخستنی database

ئەم فایلە چێک بکە:

```text
config/db.php
```

ڕێکخستنی default ـی XAMPP:

```php
$host = 'localhost';
$user = 'root';
$pass = '';
$dbname = 'pharmacy_db';
```

بۆ بەکارهێنانی ڕاستەقینە، password ـی بەتاڵ بەکارمەهێنە.

### 6. سیستەمەکە بکەرەوە

```text
http://localhost/pharmacy_xampp_redesigned/
```

---

## Login ـی demo

```text
Email: admin@pharmacy.local
Password: admin123
```

دوای login، password ـەکە دەستبەجێ بگۆڕە.

---

## فۆرماتی CSV بۆ import ـی دەرمان

ستونی پێویست:

```text
name
```

ستونە هەڵبژاردەکان:

```text
generic_name, barcode, category, min_stock, quantity, expiry_date, purchase_price, selling_price, batch_number, supplier
```

نموونەی header:

```csv
name,generic_name,barcode,category,min_stock,quantity,expiry_date,purchase_price,selling_price,batch_number,supplier
```

---

## Backup

script ـی backup بۆ macOS XAMPP هەیە:

```text
scripts/backup_database_mac_xampp.sh
```

بەدەستی بەڕێوەی ببە:

```bash
/Applications/XAMPP/xamppfiles/htdocs/pharmacy_xampp_redesigned/scripts/backup_database_mac_xampp.sh
```

backup ـەکان لێرە پاشەکەوت دەبن:

```text
/Users/Shared/pharmacy_backups
```

بۆ بەکارهێنانی ڕاستەقینە، backup پێویستە لە external drive یان cloud ـیش هەبێت.

---

## ڕێکخستنی پێشنیارکراو بۆ دەرمانخانەی ڕاستی

بۆ دەرمانخانەی ڕاستەقینە، باشترە سیستەمەکە لەسەر server یان mini PC ـی تایبەت کار بکات.

ڕێکخستنی پێشنیارکراو:

```text
Mini PC / local server
Apache یان Nginx
PHP
MariaDB
Automatic database backup
UPS بۆ پاراستنی کارەبا
Desktop browser shortcut
Barcode scanner
Receipt printer
```

بەکارهێنەران دەتوانن سیستەمەکە لە shortcut بکەنەوە:

```text
http://192.168.1.10/pharmacy/
```

بەم شێوەیە پێویست ناکات هەموو جار XAMPP بەدەستی بکرێتەوە.

---

## تێبینییەکانی Security

پێش بەکارهێنانی ڕاستی، ئەمانە بکە:

* password ـی admin بگۆڕە
* database credential ـی بەهێز بەکاربهێنە
* HTTPS چالاک بکە ئەگەر لە network یان internet بەکاردێت
* backup لە دەرەوەی کۆمپیوتەری سەرەکی هەبێت
* restore ـی database تاقی بکەوە
* permission ـی بەکارهێنەران چێک بکە
* file upload security چێک بکە
* CSRF protection چێک بکە
* audit logs چێک بکە
* debug output داخە
* `.env` و backup و database dump مەخە GitHub

پێشنیاری `.gitignore`:

```gitignore
.env
storage/backups/
*.sql
*.zip
```

---

## ئاگاداری Production

ئەم پڕۆژەیە نابێت بە تەواوی production-ready دابنرێت تا ئەمانە نەکرێن:

* security audit ـی تەواو
* چێکی workflow لەلایەن دەرمانساز
* چێکی یاسا و ڕێنمایی ناوخۆیی
* تاقیکردنەوەی backup و restore
* تاقیکردنەوەی barcode scanner
* تاقیکردنەوەی receipt printer
* تاقیکردنەوەی چەند بەکارهێنەر
* hardening ـی server

---

## Screenshot

وێنەکان لێرە زیاد بکە:

```text
screenshots/login.png
screenshots/dashboard.png
screenshots/medicines.png
screenshots/pos.png
screenshots/reports.png
```

نموونە:

```markdown
![Dashboard](screenshots/dashboard.png)
```

---

## پلانی داهاتوو

چاکسازییە پێشنیارکراوەکان:

* installer ـی تەواو بۆ Windows
* دامەزراندنی بێ XAMPP
* cloud backup integration
* ڕێنمایی HTTPS بۆ local server
* بەڕێوەبردنی خەرجییەکان
* ڕاپۆرتی net profit/loss
* چاپی barcode label
* چێکی پێشکەوتووی وەسفە
* پشتگیری چەند لقێکی دەرمانخانە
* POS ـی باشتر بۆ mobile/tablet

---

## License

ئەم پڕۆژەیە بۆ فێربوون و demo ـە.
دەتوانیت license ـی دڵخوازی خۆت زیاد بکەیت، بۆ نموونە:

```text
MIT License
```
