NethwinPOS 📚🛒

📌 Project Overview

NethwinPOS is an integrated web-based Point of Sale (POS) and Customer Reward Points Management System developed for Nethwin Bookshop.

The project addresses common problems in manual retail operations such as handwritten billing, disconnected inventory records, difficult end-of-day reconciliation, fragmented customer information, and the absence of a structured loyalty program.

The system brings these operations together through a centralized platform with role-based access for **Cashiers, Customers, Managers, Administrators, and Guest Users**.

The project follows an **Agile/Scrum development approach**, using iterative development and continuous stakeholder feedback.



✨ Key Features

🧾 Point of Sale

* Fast product lookup by name, ISBN, category, or barcode
* Shopping cart and checkout workflow
* Stock verification during checkout
* Subtotal, tax, discount, and total calculations
* Cash and card payment support
* Receipt generation
* Receipt download/printing support
* Return and refund workflow
* Barcode/camera scanner support

📦 Inventory & Catalog Management

* Book and stationery product management
* ISBN-based book cataloguing
* Barcode/SKU-based stationery handling
* Add, edit, and deactivate products
* Stock quantity tracking
* Automatic stock updates after sales and returns
* Low-stock monitoring and alerts
* Product categories and filtering
* Product image upload and cloud storage support

🎁 Customer Reward Points

* Automatic reward points calculation
* Reward point balance tracking
* Redeeming points during checkout
* Points transaction history
* Configurable earning and redemption rules
* Membership tier support
* Tier-based earning multipliers and benefits

👤 Customer Portal

* Customer registration and login
* Profile management
* Reward point balance
* Purchase/transaction history
* Membership tier information
* Pre-order placement
* Order and loyalty notifications

📚 Pre-Orders

* Place pre-orders for out-of-stock or upcoming books
* Manage pre-order status
* Track reserved items
* Notify customers when products become available

📊 Management & Analytics

* Manager dashboard
* Sales analytics and reporting
* Revenue and transaction monitoring
* Product performance information
* Customer loyalty analytics
* Financial reporting with date-range filtering
* Administrative user management

🔐 Authentication & Security

* Secure user authentication
* Password hashing
* JWT-based authentication
* Role-Based Access Control (RBAC)
* User account activation/deactivation
* Protected management endpoints
* Payment webhook signature verification
* Environment variables for sensitive configuration

☁️ External Services

* **Cloudinary** for product image/report storage
* **Stripe** for online payment processing
* **Email service** for transactional notifications
* **Redis/ARQ** support for background jobs



👥 User Roles

| Role              | Main Capabilities                                                                                  |
| ----------------- | -------------------------------------------------------------------------------------------------- |
| **Guest**         | View shop information, browse products, register an account                                        |
| **Customer**      | Purchase products, view reward balance, view history, redeem points, place pre-orders              |
| **Cashier**       | Process POS sales, apply reward points, generate receipts, handle returns/refunds                  |
| **Manager**       | Manage inventory, monitor sales, manage promotions, view reports, manage loyalty settings          |
| **Administrator** | Manage users, configure the system and reward program, access administration functions and reports |



🏗️ System Architecture

NethwinPOS uses a layered web application architecture:

```text
┌──────────────────────────────────────────────┐
│              Presentation Layer              │
│      React / TypeScript + Tailwind CSS       │
│                                              │
│  Customer UI • POS • Catalog • Dashboards    │
└───────────────────────┬──────────────────────┘
                        │ REST API / JSON
                        ▼
┌──────────────────────────────────────────────┐
│               Application Layer              │
│              Python + FastAPI                │
│                                              │
│ Auth • POS • Orders • Inventory • Loyalty    │
│ Pre-orders • Users • Analytics • Payments    │
└───────────────────────┬──────────────────────┘
                        │
                        ▼
┌──────────────────────────────────────────────┐
│                    Data Layer                │
│                   MongoDB                    │
│                                              │
│ Users • Products • Orders • Customers        │
│ Loyalty Transactions • Categories            │
└──────────────────────────────────────────────┘

              External Integrations
        ┌──────────┬───────────┬──────────┐
        ▼          ▼           ▼          ▼
    Cloudinary   Stripe      Email      Redis/ARQ
```



🛠️ Technology Stack

Frontend

* **React.js**
* **TypeScript**
* **Tailwind CSS**
* React Hook Form
* Zod validation
* TanStack React Query
* Lucide React

Backend

* **Python**
* **FastAPI**
* Pydantic / Pydantic Settings
* FastAPI Users
* JWT authentication
* RESTful APIs

Database

* **MongoDB**
* Beanie ODM
* Motor async MongoDB driver
* MongoDB Compass

Integrations & Services

* **Stripe** – payment processing
* **Cloudinary** – media/file storage
* **Redis / ARQ** – background job support
* Email service – transactional messages and notifications

Development & Collaboration

* Git
* GitHub
* Postman
* Figma
* Google Meet / WhatsApp



📁 Main Project Modules

```text
Authentication & Users
├── Login / Registration
├── Password Reset
├── JWT Authentication
└── Role-Based Access Control

Catalog & Inventory
├── Books
├── Stationery
├── Categories
├── Catalog Search
└── Stock Management

Sales & Orders
├── Cart
├── POS Checkout
├── Orders
├── Payments
├── Receipts
└── Returns / Refunds

Customer Loyalty
├── Reward Points
├── Membership Tiers
├── Points Transactions
└── Redemption

Customer Services
├── Pre-Orders
├── Email Notifications
└── Customer Accounts

Management
├── Analytics
├── Reports
├── User Administration
└── System Configuration
```



🔄 Main Business Flow

```text
Customer / Cashier
        │
        ▼
   Product Search
        │
        ▼
   Add to Cart
        │
        ▼
  Checkout & Pricing
        │
        ├──────────────► Redeem Reward Points
        │
        ▼
      Payment
        │
        ▼
   Order Confirmation
        │
        ├──────────────► Update Inventory
        ├──────────────► Award Reward Points
        └──────────────► Generate Receipt / Email
```



🎯 Project Objectives

* Build a fast and accurate POS checkout interface
* Automate inventory management and stock updates
* Introduce an integrated customer reward points engine
* Centralize customer information and purchase history
* Implement secure role-based access control
* Automate receipt and invoice generation
* Provide dashboards and sales analytics for management
* Support responsive interfaces using Tailwind CSS
* Provide pre-order and membership functionality
* Deliver the system using an Agile development process



## 👩‍💻 My Contribution – Hansani Premathilaka

Role: Start-Up Manager

My primary development responsibilities included:

* Designing and implementing the Sign Up & Login Module
* Developing the **Manager Dashboard**
* Contributing to project start-up documentation and stakeholder planning
* Supporting requirements, acceptance criteria, and project success definitions
* Collaborating with the team through Git/GitHub and Agile development practices




🧪 Testing Approach

The project testing strategy includes:

* Unit testing
* Integration testing
* Backend API testing with Postman
* Frontend component testing
* Functional testing against user-story acceptance criteria
* Authentication and RBAC testing
* User Acceptance Testing (UAT)
* End-to-end testing
* Bug fixing and final validation



📅 Development Methodology

NethwinPOS was developed using an Agile methodology with Scrum practices.

Key practices include:

* Sprint Planning
* Daily Stand-ups
* Sprint Reviews
* Sprint Retrospectives
* Continuous Integration using Git/GitHub
* Continuous client feedback

Development was organized around incremental delivery of:



🔒 Security Considerations

Security features and practices include:

* HTTPS in production
* Secure password storage
* JWT authentication
* Role-Based Access Control
* Protected administrative endpoints
* Payment webhook signature verification
* Environment variables for sensitive configuration



📚 Documentation

Project documentation includes:

* Project Proposal
* System Architecture Diagram
* Use Case Diagram
* User Stories
* Database Design
* Work Breakdown Structure (WBS)
* Product Breakdown Structure (PBS)
* Gantt Chart
* Testing Strategy
* Risk Management Documentation
* API Documentation
* User Documentation


🌱 Future Enhancements

Potential future extensions include:

* SMS promotional notifications
* Additional payment gateway integrations
* Multi-branch support
* Expanded analytics and business intelligence
* Advanced customer promotions
* Supplier integration
* Online sales and e-commerce expansion



## 📄 Project Information

| Item             | Details                                                      |
| ---------------- | ------------------------------------------------------------ |
| **Project Name** | NethwinPOS                                                   |
| **Project Type** | Web-Based Point of Sale & Customer Loyalty Management System |
| **Domain**       | Bookshop & Stationery Retail                                 |
| **Methodology**  | Agile / Scrum                                                |
| **Frontend**     | React.js / TypeScript / Tailwind CSS                         |
| **Backend**      | Python / FastAPI                                             |
| **Database**     | MongoDB                                                      |
| **Storage**      | Cloudinary                                                   |
| **Payments**     | Stripe                                                       |





⭐ Acknowledgement

NethwinPOS was developed as a collaborative academic software project to explore:

* Modern web application development
* Retail automation
* Customer loyalty management
* API development
* Database management
* Agile project management
* Secure system design
* User-centered interface development

