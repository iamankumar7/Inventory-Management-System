
🎯 Overview
Inventory Management System is an enterprise-grade Spring Boot application designed for comprehensive inventory tracking across multiple warehouses. It provides complete functionality for managing products, stock levels, suppliers, purchases, sales, and inter-warehouse transfers with advanced features like batch tracking, expiry management, and inventory valuation.

This project demonstrates:

Multi-warehouse inventory management
Complex JPA entity relationships
RESTful API design with comprehensive endpoints
Service layer architecture with business logic
Advanced querying and reporting capabilities
✨ Features
Core Features
✅ Multi-Warehouse Support - Track inventory across multiple warehouse locations
✅ Product Management - Comprehensive product catalog with SKU and barcode support
✅ Stock Tracking - Real-time stock levels with batch and lot number tracking
✅ Supplier Management - Vendor management with ratings and payment terms
✅ Purchase Orders - Complete purchase order lifecycle management
✅ Sales Orders - Sales order processing with payment tracking
✅ Stock Transfers - Inter-warehouse stock transfer with approval workflow
Advanced Features
📊 Inventory Valuation - Support for FIFO, LIFO, and Average costing methods
📅 Expiry Tracking - Batch and expiry date management for perishable goods
🔔 Low Stock Alerts - Automatic alerts when stock falls below reorder levels
📈 Analytics Ready - Date range queries for reporting and forecasting
🏷️ Barcode/QR Support - Product identification via barcode scanning
💰 Financial Tracking - Cost price, selling price, and profit margin tracking
🛠️ Tech Stack
Technology	Version	Purpose
Java	21	Programming Language
Spring Boot	4.0.1	Application Framework
Spring Data JPA	4.0.1	Data Access Layer
Hibernate	(via Spring Boot)	ORM Framework
MySQL	8.0+	Relational Database
Maven	4.0.0	Build Tool
Spring Boot DevTools	4.0.1	Development Utilities
📦 Entities
1. Product
Represents items in the inventory system

Product information (name, SKU, barcode, description)
Pricing (cost price, selling price)
Category and unit of measurement
Reorder level for low stock alerts
2. Warehouse
Represents storage locations

Warehouse identification (code, name)
Location details (address, city, state, country)
Contact information
Capacity tracking
Active/inactive status
3. Stock
Tracks inventory levels in warehouses

Product-warehouse relationship
Quantity tracking
Batch and lot number
Expiry and manufacturing dates
Valuation method (FIFO/LIFO/Average)
4. Supplier
Manages vendor information

Supplier details (code, name, contact)
Payment terms and credit limit
Rating system (1-5 stars)
Active/inactive status
5. Purchase
Purchase order management

Order tracking (PO number, dates)
Supplier and product relationship
Quantity and pricing
Order status (Pending, Confirmed, Shipped, Delivered, Cancelled)
Batch and expiry tracking
6. Sale
Sales order processing

Order tracking (SO number, dates)
Customer information
Quantity, pricing, discount, and tax
Payment status (Unpaid, Partially Paid, Paid, Refunded)
Order status (Pending, Confirmed, Processing, Shipped, Delivered, Cancelled, Returned)
7. Transfer
Inter-warehouse stock transfers

Transfer tracking (transfer number, dates)
Source and destination warehouses
Product and quantity
Transfer status (Pending, Approved, In Transit, Received, Cancelled, Rejected)
Approval workflow (initiated by, approved by, received by)
🚀 Getting Started
Prerequisites
Java Development Kit (JDK) 21 or higher
Maven 3.6+
MySQL 8.0+ installed and running
Git for cloning the repository
Installation
Clone the repository

git clone https://github.com/Dronanaik/Java_Backend.git
cd Java_Backend/InventoryManagement
Create MySQL Database

mysql -u root -p
Then execute:

CREATE DATABASE inventory_management;
EXIT;
Configure Database Connection

Edit src/main/resources/application.properties:

spring.datasource.username=your_mysql_username
spring.datasource.password=your_mysql_password
Install Dependencies

mvn clean install
Running the Application
mvn spring-boot:run
The application will start on http://localhost:8080
