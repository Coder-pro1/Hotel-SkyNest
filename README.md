# 🏨 Hotel SkyNest Management System

<div align="center">

**A comprehensive hotel management system with role-based dashboards, real-time billing, and advanced financial management**

[![React](https://img.shields.io/badge/React-18-blue.svg)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-16+-green.svg)](https://nodejs.org/)
[![MySQL](https://img.shields.io/badge/MySQL-8.0+-orange.svg)](https://www.mysql.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

[Features](#-features) • [Installation](#-installation) • [API Docs](#-api-documentation)

</div>

---

## 📸 Dashboard Gallery

<div align="center">

### Login Interface
![Login Page](readme_photos/login_page.png)

### Admin Dashboard
![Admin Dashboard](readme_photos/admin_dashboard.png)
*Complete system control: User management, branch configuration, financial settings, and comprehensive reports*

### Receptionist Dashboard
![Receptionist Dashboard](readme_photos/receptionist_dashboard.png)
*Day-to-day operations: Booking management, check-in/out, payment processing, and service requests*

### Guest Dashboard
![Guest Dashboard](readme_photos/guest_dashboard.png)
*Guest portal: View bookings, request services, track payments, and manage profile*

### Key Features

![Booking Management](readme_photos/booking.png)
*Real-time booking system with availability checking and automatic pricing*

![Guest Bill View](readme_photos/guest_bill.png)
*Detailed bill breakdown with room charges, services, taxes, discounts, and payment history*

</div>

---

## ✨ Features

- 🎯 **Role-Based Access Control** - Admin, Receptionist, and Guest dashboards with specific permissions
- 💰 **Advanced Financial System** - Flexible tax, discount, and fee management per branch
- 📊 **Real-Time Billing** - Live bill calculation with automatic updates for services, taxes, and fees
- 🛎️ **Service Management** - Room service, housekeeping, maintenance requests with usage tracking
- 📈 **Comprehensive Reporting** - Revenue, occupancy, service trends, and unpaid booking reports
- 🔐 **Secure Authentication** - JWT-based auth with password hashing and email verification
- 🐳 **Docker Ready** - Multi-container setup with Docker Compose for easy deployment
- ☁️ **Railway Deployable** - Cloud deployment configuration included

## 🚀 Installation

### Docker Setup (Recommended)

```bash
# Clone repository
git clone https://github.com/yourusername/Hotel-SkyNest.git
cd Hotel-SkyNest

# Start with Docker Compose
docker-compose up -d
```

Access:
- **Frontend**: http://localhost
- **Backend API**: http://localhost:5000

### Railway Deployment

1. Connect GitHub repo to [Railway](https://railway.app/)
2. Add MySQL database service
3. Set environment variables: `JWT_SECRET`, `NODE_ENV=production`
4. Railway auto-deploys on push
5. Initialize database using Railway Data tab

### Local Development

```bash
# Database setup
mysql -u root -p
CREATE DATABASE skynest_hotels;
exit
mysql -u root -p skynest_hotels < database/COMPLETE_DATABASE_SETUP.sql

# Backend
cd backend
npm install
npm start  # http://localhost:5000

# Frontend (new terminal)
cd frontend
npm install
npm run dev  # http://localhost:5173
```

**Default Login:**
- Admin: `admin@skynest.com` / `admin123`
- Receptionist: `receptionist@skynest.com` / `receptionist123`
- Guest: `guest@skynest.com` / `guest123`



## 🛠️ Tech Stack

**Frontend:** React 18, Vite, React Router, Axios, CSS3, Lucide Icons  
**Backend:** Node.js, Express.js, MySQL2, JWT, bcrypt  
**Database:** MySQL 8.0+ with stored procedures, triggers, and views  
**DevOps:** Docker, Docker Compose, Nginx, Railway

## 🗄️ Database & Architecture

**Core Tables:** Users, Branches, Rooms, Bookings, Guests, Payments, Services, Taxes, Discounts, Fees, Support Tickets  
**Key Features:** Stored procedures for complex logic, automatic tax/discount calculation, real-time billing, audit logging

**Payment System:**
- Multiple payment methods (cash, card, bank transfer, online)
- Flexible tax configuration (VAT, Service Tax, custom taxes)
- Discount types: percentage, fixed amount, early bird, loyalty, seasonal
- Fee management: late checkout, early checkin, cancellation, damage fees
- Live bill calculation with automatic updates

## 📚 API Documentation

Complete REST API with role-based access control:

**Main Endpoints:**
- `/api/auth` - Authentication (register, login, email verification, password reset)
- `/api/users` - User management (Admin only)
- `/api/branches` - Hotel branch management
- `/api/rooms` - Room management and availability checking
- `/api/bookings` - Booking CRUD, check-in/out, live bill
- `/api/guests` - Guest registration and history
- `/api/payments` - Payment processing, receipts, refunds
- `/api/services` - Service catalogue management
- `/api/service-requests` - Service request handling
- `/api/tax-discount` - Tax and discount configuration
- `/api/fees` - Fee management
- `/api/support` - Support ticket system
- `/api/reports` - Revenue, occupancy, service, and financial reports

**Key Features:**
- JWT authentication on protected routes
- Role-based authorization (Admin, Receptionist, Guest)
- Real-time bill calculation endpoint
- Comprehensive reporting endpoints
- Payment breakdown and receipt generation

## 🤝 Contributing

Contributions welcome! Fork the repo, create a feature branch, commit changes, and open a Pull Request.

## 📝 License

MIT License - see LICENSE file for details.

## 📞 Support

- **GitHub Issues**: [Report bugs or request features](https://github.com/yourusername/Hotel-SkyNest/issues)
- **Email**: support@hotelskynest.com

---

<div align="center">

**Built with ❤️ for modern hotel management**

⭐ Star us on GitHub!

[Report Bug](https://github.com/yourusername/Hotel-SkyNest/issues) · [Request Feature](https://github.com/yourusername/Hotel-SkyNest/issues)

</div>
