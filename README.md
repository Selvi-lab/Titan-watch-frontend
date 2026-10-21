# Titan Watch Store - Full Stack E-Commerce Website

A modern and attractive watch shopping website built with React.js, Python Flask, and MySQL. The project demonstrates a complete full-stack e-commerce solution with user shopping features, admin panel, product management, and coupon validation.

## 📋 Project Overview

**Titan Watch** is a beginner-friendly full-stack web application that showcases:
- Frontend: React.js with responsive UI
- Backend: Python Flask REST API
- Database: MySQL
- Admin Panel: Product CRUD operations, purchase tracking, coupon management

## ✨ Features

### User Features
- **Home Page**: Hero banner, product categories, featured products
- **Products Page**: Browse all products, filter by category
- **Product Details**: View detailed product information
- **Shopping Cart**: Add products and proceed to checkout
- **Coupon System**: Guess a number (0-9) to validate coupon during checkout
- **Purchase**: Complete purchase with customer information
- **Responsive Design**: Works on desktop, tablet, and mobile devices

### Admin Features
- **Admin Login**: Secure login with demo credentials
- **Coupon Management**: View and manage coupon codes
- **Product Management**: 
  - Add new products
  - View all products
  - Edit product details
  - Delete products
- **Purchase History**: Track all customer purchases

## 🛠️ Tech Stack

### Frontend
- **React.js** - UI framework
- **React Router** - Client-side routing
- **Axios** - HTTP client
- **CSS3** - Styling with responsive design

### Backend
- **Python 3.x** - Programming language
- **Flask** - Web framework
- **Flask-CORS** - Cross-origin support
- **Flask-MySQLdb** - Database connector

### Database
- **MySQL** - Relational database

## 📁 Project Structure

```
titan-watch-website/
├── frontend/                    # React application
│   ├── public/
│   │   └── index.html          # HTML template
│   ├── src/
│   │   ├── components/         # React components
│   │   │   ├── Navbar.js
│   │   │   ├── Footer.js
│   │   │   └── ProductCard.js
│   │   ├── pages/              # Page components
│   │   │   ├── HomePage.js
│   │   │   ├── ProductsPage.js
│   │   │   ├── ProductDetailPage.js
│   │   │   ├── CheckoutPage.js
│   │   │   ├── AdminLoginPage.js
│   │   │   └── AdminPanel.js
│   │   ├── styles/             # CSS files
│   │   ├── App.js              # Main app component
│   │   └── index.js            # Entry point
│   └── package.json            # Dependencies
├── backend/                     # Flask application
│   ├── app.py                  # Main Flask app
│   ├── requirements.txt        # Python dependencies
│   └── .env                    # Environment variables
└── database/
    └── setup.sql               # Database schema
```

## 🚀 Getting Started

### Prerequisites
- Node.js (v14 or higher)
- Python 3.x
- MySQL Server
- npm or yarn

### 1. Database Setup

```bash
# Open MySQL and run the setup script
mysql -u root -p < database/setup.sql

# Or if you have a password
mysql -u root -p<password> < database/setup.sql
```

This creates:
- Database: `titan_watch`
- Tables: categories, products, purchases, admin_users
- Sample data: 9 products, 3 categories

### 2. Backend Setup

```bash
# Navigate to backend directory
cd backend

# Create virtual environment (optional but recommended)
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Configure database connection in .env
# Edit .env file with your MySQL credentials:
# DB_HOST=localhost
# DB_USER=root
# DB_PASSWORD=your_password
# DB_NAME=titan_watch

# Run Flask server
python app.py
```

The backend will start at `http://localhost:5000`

### 3. Frontend Setup

```bash
# Navigate to frontend directory
cd frontend

# Install dependencies
npm install

# Start development server
npm start
```

The frontend will start at `http://localhost:3000`

## 📱 User Flow

### Customer Journey
1. **Home Page** → Browse products and categories
2. **Products Page** → Filter by category (Men, Women, Smart Watches)
3. **Product Detail** → View product information
4. **Checkout** → Enter customer details
5. **Coupon Validation** → Guess coupon number (0-9)
6. **Purchase Confirmation** → Order saved to database

### Admin Flow
1. **Admin Login** → Enter credentials
2. **Admin Panel** → Access management features
3. **Coupon Display** → View current coupon number
4. **Product Management** → Add, view, or delete products
5. **Purchase History** → Track all customer orders

## 🔑 Demo Credentials

### Admin Login
- **Email**: `admin@titanwatch.com`
- **Password**: `admin123`

## 📝 API Endpoints

### Products
- `GET /api/products` - Get all products
- `GET /api/products/<id>` - Get single product
- `GET /api/products/featured?limit=6` - Get featured products
- `GET /api/products/category/<category>` - Get by category
- `POST /api/products` - Add new product (Admin)
- `DELETE /api/products/<id>` - Delete product (Admin)

### Categories
- `GET /api/categories` - Get all categories

### Coupon
- `GET /api/coupon` - Get current coupon
- `POST /api/coupon/validate` - Validate guess

### Admin
- `POST /api/admin/login` - Admin login

### Purchases
- `GET /api/purchases` - Get all purchases
- `POST /api/purchases` - Create new purchase

## 🎨 Design Features

- **Modern UI**: Clean, professional design with gradients
- **Responsive Layout**: Mobile-first approach
- **Color Scheme**: Deep blue (#1a1a2e), red (#e74c3c), gradients
- **Smooth Animations**: Hover effects and transitions
- **Professional Cards**: Product cards with hover effects

## 🔒 Security Features

- **Admin Authentication**: Email/password validation
- **CORS Enabled**: Cross-origin requests handled
- **Database Queries**: Parameterized queries to prevent SQL injection
- **Secure Checkout**: Form validation and error handling

## 📦 Sample Data

The database includes:
- **3 Watch Categories**: Men, Women, Smart Watches
- **9 Sample Products**: 3 in each category with images and descriptions
- **1 Admin User**: Demo credentials

## 🐛 Troubleshooting

### Database Connection Error
```
Error: Database connection failed
Solution: Check MySQL is running and credentials in .env match
```

### Port Already in Use
```
Error: Address already in use
Solution: Change port in backend/app.py or kill existing process
```

### CORS Error
```
Error: CORS policy blocked request
Solution: Ensure Flask-CORS is installed and app is configured correctly
```

### Module Not Found
```
Error: No module named 'MySQLdb'
Solution: Run pip install Flask-MySQLdb
```

## 📚 Learning Outcomes

This project demonstrates:
- React component structure and hooks
- REST API design with Flask
- MySQL database design
- Frontend-backend integration
- User authentication
- CRUD operations
- Responsive web design
- Error handling

## 🎓 For Beginners

This project is designed for beginners and includes:
- Clear file structure
- Well-commented code
- Simple database schema
- Basic authentication
- No advanced frameworks
- Demo credentials for testing

## 📄 License

This project is open source and available for educational purposes.

## 🤝 Contributing

Feel free to fork, modify, and improve this project as a learning exercise.

## 📞 Support

For issues or questions:
1. Check the README troubleshooting section
2. Review the API endpoints documentation
3. Check browser console for error messages
4. Verify database connection and credentials

---

**Created for CyberCodersHub**
**Generated: September 1, 2024**
# Titan-watch-frontend
