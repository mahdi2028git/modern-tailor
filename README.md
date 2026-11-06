# modern-tailor
✂️ Modern Tailor
A modern tailoring shop management system built with Laravel. Manage customers, measurements, orders, fittings, payments, and staff from one clean dashboard.

Laravel PHP License PRs Welcome Live Demo

🔗 Live Demo: https://claude.ai/artifact/Fuvr36LxT61pHXUGeMQgzr

Demo login: admin@moderntailor.test / password

📖 Table of Contents
Live Demo
Features
Screenshots
Tech Stack
Requirements
Installation
Configuration
Usage
Project Structure
Testing
Roadmap
Contributing
License
🌐 Live Demo
Try the app online: https://claude.ai/artifact/Fuvr36LxT61pHXUGeMQgzr

Role	Email	Password
Admin	admin@moderntailor.test	password
The demo data resets periodically. Please don't enter real personal information.

✨ Features
Customer Management – Profiles, contact info, order history, and notes
Measurement Records – Store and update body measurements per customer, with version history
Order Management – Create orders for suits, shirts, dresses, alterations, and more
Order Tracking – Status pipeline: Received → Cutting → Stitching → Fitting → Ready → Delivered
Fabric & Inventory – Track fabrics, buttons, threads, and low-stock alerts
Payments & Invoicing – Advance payments, balance due, printable invoices (PDF)
Appointments – Schedule fittings and pickups
Staff & Roles – Admin, manager, tailor, and cashier permissions
Notifications – Email/SMS alerts when orders are ready
Reports & Analytics – Sales, pending orders, top customers, and revenue charts
Responsive UI – Works on desktop, tablet, and mobile
📸 Screenshots
Add your screenshots to a /docs/screenshots folder and update the links below.

Dashboard	Order Details
Dashboard	Order
🛠 Tech Stack
Layer	Technology
Backend	Laravel 11, PHP 8.2+
Frontend	Blade, Tailwind CSS, Alpine.js
Database	MySQL 8 / MariaDB / PostgreSQL
Build Tool	Vite
Auth	Laravel Breeze / Sanctum
PDF	barryvdh/laravel-dompdf
Testing	Pest / PHPUnit
📋 Requirements
PHP >= 8.2
Composer >= 2.x
Node.js >= 18 and npm
MySQL 8+ (or compatible database)
PHP extensions: mbstring, xml, curl, pdo, bcmath, gd
🚀 Installation
# 1. Clone the repository
git clone https://github.com/your-username/modern-tailor.git
cd modern-tailor

# 2. Install PHP dependencies
composer install

# 3. Install JS dependencies
npm install

# 4. Set up environment file
cp .env.example .env

# 5. Generate application key
php artisan key:generate

# 6. Configure your database in .env, then run migrations and seeders
php artisan migrate --seed

# 7. Link storage
php artisan storage:link

# 8. Build assets
npm run build   # or: npm run dev

# 9. Start the server
php artisan serve
Visit http://localhost:8000 in your browser.

⚙️ Configuration
Update the following in your .env file:

APP_NAME="Modern Tailor"
APP_URL=http://localhost:8000

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=modern_tailor
DB_USERNAME=root
DB_PASSWORD=

MAIL_MAILER=smtp
MAIL_HOST=smtp.mailtrap.io
MAIL_PORT=2525
MAIL_USERNAME=
MAIL_PASSWORD=
MAIL_FROM_ADDRESS="hello@moderntailor.test"
MAIL_FROM_NAME="${APP_NAME}"
Default Admin Login (after seeding)
Email	Password
admin@moderntailor.test	password
⚠️ Change these credentials immediately in production.

💡 Usage
Log in as admin.
Add a customer and record their measurements.
Create an order, pick garment type, fabric, and delivery date.
Record advance payment and generate an invoice.
Update order status as work progresses; customers get notified when ready.
View reports from the dashboard to track business performance.
Useful Commands
php artisan migrate:fresh --seed   # Reset database with demo data
php artisan queue:work             # Process queued notifications
php artisan schedule:work          # Run scheduled tasks locally
php artisan optimize:clear         # Clear all caches
📂 Project Structure
modern-tailor/
├── app/
│   ├── Http/Controllers/
│   ├── Models/            # Customer, Measurement, Order, Fabric, Payment...
│   ├── Policies/
│   └── Notifications/
├── database/
│   ├── migrations/
│   ├── factories/
│   └── seeders/
├── resources/
│   ├── views/
│   ├── css/
│   └── js/
├── routes/
│   ├── web.php
│   └── api.php
├── tests/
└── README.md
🧪 Testing
php artisan test
# or
./vendor/bin/pest
🗺 Roadmap
 Customer self-service portal
 WhatsApp / SMS integration
 Online payment gateway (Stripe / PayPal)
 Barcode / QR code order tags
 Multi-branch support
 REST API with mobile app
 Multi-language support
🤝 Contributing
Contributions are welcome!

Fork the repository
Create a feature branch: git checkout -b feature/amazing-feature
Commit your changes: git commit -m "Add amazing feature"
Push to the branch: git push origin feature/amazing-feature
Open a Pull Request
Please follow PSR-12 coding standards and include tests where possible.

🔒 Security
If you discover a security vulnerability, please email security@yourdomain.com instead of using the issue tracker.

📄 License
This project is open-source software licensed under the MIT License.

🙌 Acknowledgements
Laravel
Tailwind CSS
Alpine.js
Made with ❤️ using Laravel