---

# 📊 Sales Analytics Dashboard

## 🚀 Overview

A high-performance, enterprise-grade sales analytics platform that processes **700,000+ records in real-time** with lightning-fast filtering, searching, and pagination.
Built with modern technologies and optimized for massive datasets, this dashboard provides **actionable insights with millisecond response times**.

---

## ✨ Key Features

### 🎯 High-Performance Architecture

* 700,000+ records processed with **sub-second response times**
* Optimized MongoDB queries with **indexed sorting and filtering**
* **Server-side pagination** that works flawlessly up to 76,800+ pages
* Intelligent caching for **filter options and frequently accessed data**

---

### 🔍 Smart Search & Filtering

* Multi-field search across **12+ fields (case-insensitive)**
* Real-time filtering with **8+ filter categories**
* Range-based filtering for **dates, ages, and amounts**
* Combined **search + filter operations** with instant results

---

### 📱 Responsive Design

* **Mobile-first approach** with perfect mobile/desktop experience
* Glass morphism UI with **dark/light mode support**
* Collapsible sidebar with intuitive navigation
* Horizontal-scroll optimized tables for mobile devices

---

### 📊 Data Visualization

* Interactive sales table with **12+ data columns**
* Real-time statistics cards showing **key metrics**
* Sortable columns with visual indicators
* **Copy-to-clipboard** functionality for phone numbers

---

## 🛠 Tech Stack

### Backend (Node.js + Express)

* Node.js 20.x
* Express.js 4.x
* MongoDB with Mongoose
* Advanced indexing strategies
* Query optimization for large datasets
* RESTful API design

### Frontend (React.js)

* React 18.x with Hooks
* Axios for API communication
* CSS3 with custom properties
* Responsive design framework
* Debounced search implementation
* Real-time state management

### Database (MongoDB Atlas)

* 700,000+ records (**230MB dataset**)
* Comprehensive indexing (**15+ indexes**)
* Aggregation pipeline optimization
* Connection pooling and timeout management

---

## 🚦 Quick Start

### 1. Prerequisites

```bash
node --version      # v20.x or higher
mongosh --version   # MongoDB installed or Atlas account
```

### 2. Backend Setup

```bash
# Clone repository
git clone <repository-url>
cd sales-dashboard

# Install dependencies
cd backend
npm install

# Environment configuration
cp .env.example .env
# Add your MongoDB URI inside .env

# Create database indexes (CRITICAL for performance)
npm run create-indexes

# Start development server
npm run dev
# Server runs on http://localhost:5000
```

### 3. Frontend Setup

```bash
cd frontend
npm install
npm start
# Dashboard opens at http://localhost:3000
```

### 4. Database Setup

```bash
# Import your sales data (CSV/JSON)
mongoimport --uri="your-mongodb-uri" \
--collection=sales_data --file=sales_data.json

# Or use the provided script
npm run import-data
```

---

## 📁 Project Structure

```
sales-dashboard/
├── backend/
│   ├── src/
│   │   ├── config/
│   │   │   └── database.js          # MongoDB connection with optimizations
│   │   ├── controllers/
│   │   │   └── salesController.js   # API endpoint handlers
│   │   ├── models/
│   │   │   └── Sales.js             # Mongoose schema with 15+ indexes
│   │   ├── routes/
│   │   │   └── salesRoutes.js       # API routes with optimized endpoints
│   │   ├── services/
│   │   │   └── salesService.js      # Business logic with query optimization
│   │   └── index.js                 # Express server setup
│   ├── create-indexes.js            # Database index creation script
│   └── package.json
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── Sidebar.jsx          # Collapsible navigation
│   │   │   ├── SearchBar.jsx        # Debounced search component
│   │   │   ├── FilterPanel.jsx      # Multi-criteria filter panel
│   │   │   ├── SalesTable.jsx       # 12-column responsive table
│   │   │   ├── Pagination.jsx       # Smart pagination controls
│   │   │   └── StatsCards.jsx       # Real-time metrics display
│   │   ├── App.jsx                  # Main application component
│   │   └── index.js                 # React entry point
│   └── package.json
└── README.md
```

---

## 🎮 Usage Guide

### 🔎 Searching Data

* Search by **customer name, phone number, transaction ID, or employee name**
* Case-insensitive search across multiple fields
* Real-time results with **500ms debounce**
* Supports partial matches and numeric searches

---

### 🧩 Applying Filters

* **Region Filter:** Single/multiple selections
* **Demographic Filters:** Gender, age range
* **Product Filters:** Category, tags
* **Transaction Filters:** Payment method, date range
* Combine multiple filters simultaneously
* **Reset:** One-click clear all

---

### ↕ Sorting Data

* Click column headers for immediate sorting
* Dropdown sort for predefined combinations
* Sort options:

  * Date, Amount, Quantity
  * Name, Age
* Visual indicators for **active sort + direction**

---

### 📄 Navigating Pages

* Direct page jump: enter any page number **(1–76,800+)**
* Smart pagination: adjacent pages with ellipsis
* Controls: **First, Last, Previous, Next**
* Record counter shows: **"Showing X–Y of Z"**

---

### 📱 Mobile Experience

* Hamburger menu for navigation
* Horizontal-scroll tables with sticky headers
* Responsive filter panel that adapts to screen size
* Touch-optimized UI components

---
