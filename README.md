# Marketplace

🛍️ Multi-Vendor Marketplace
This is a full-stack Multi-Vendor Marketplace application built with the MERN (MongoDB, Express.js, React.js, Node.js) stack. It allows multiple independent vendors to list and sell their products, while customers can browse, purchase, and review items from various sellers. An administrative panel provides overall platform control and management.

✨ Features
The marketplace offers distinct functionalities tailored for Customer, Vendor, and Admin roles.

Customer Features
User Authentication: Secure registration, login, and password reset.

Product Browsing & Search: Explore products, filter by category, price, vendor, and ratings.

Product Details: View comprehensive product information, images, and customer reviews.

Shopping Cart: Add, remove, and update product quantities before checkout.

Secure Checkout: Integrated payment processing (via Stripe) and shipping address management.

Order History: Track past and current orders with status updates.

User Profile: Manage personal information and saved shipping addresses.

Reviews & Ratings: Submit feedback and ratings for purchased products.

Vendor Features
Vendor Onboarding: Application process for new sellers, requiring admin approval.

Vendor Dashboard: Overview of sales, orders, and product performance.

Product Management: CRUD (Create, Read, Update, Delete) operations for products, including inventory management and image uploads.

Order Management: View new orders, update order statuses (e.g., shipped, delivered).

Vendor Profile: Manage store branding and details.

Admin Features
Admin Dashboard: Centralized platform overview with key metrics.

User Management: Manage all customer and vendor accounts, including role changes and vendor application approvals.

Product Moderation: Review and approve new product listings, or remove inappropriate content.

Category Management: CRUD operations for product categories.

Order Oversight: View all orders across the entire platform.

Reporting: Access to sales reports and user activity logs.

🛠️ Technology Stack
The project leverages the power of the MERN stack for a robust and scalable solution.

Frontend (Client-Side)
React.js: A JavaScript library for building dynamic user interfaces.

Tailwind CSS: A utility-first CSS framework for rapid and responsive UI development.

Zustand / React Context API: For efficient global state management.

Lucide-React / Inline SVGs: For a consistent icon set.

Shadcn/ui: Reusable UI components for a polished user experience.

Backend (Server-Side)
Node.js: A JavaScript runtime for building scalable server-side applications.

Express.js: A fast, unopinionated, minimalist web framework for Node.js.

Mongoose: An ODM (Object Data Modeling) library for MongoDB.

JSON Web Tokens (JWT): For secure and stateless user authentication.

bcrypt.js: For hashing and comparing passwords securely.

multer: Middleware for handling multipart/form-data, primarily for file uploads (e.g., product images).

Stripe API: Integrated for secure payment processing.

express-validator / Joi: For robust input validation.

Database
MongoDB: A flexible, document-based NoSQL database for storing all application data.

🏛️ System Architecture
The application follows a client-server architecture. The React.js frontend interacts with the Node.js/Express.js backend via RESTful APIs. The backend handles business logic, authentication, and communicates with the MongoDB database for data persistence. External services like Stripe are integrated with the backend for specific functionalities (e.g., payments). Image uploads will ideally be handled by a cloud storage service (e.g., AWS S3, Cloudinary) with only URLs stored in MongoDB.

🚀 Project Flow
The marketplace accommodates three main user roles, each with distinct interaction flows:

Customer Flow:

Authentication (Register/Login) → Browse/Search Products → View Product Details → Add to Cart → View Shopping Cart → Proceed to Checkout → Enter Payment Details (Stripe) → Place Order → Order Confirmation → View Order History.

Vendor Flow:

Authentication (Login) → Access Vendor Dashboard → Product Management (Add/Edit/Delete Products, Image Upload) → Order Management (View/Update Order Status) → Profile Settings.

Admin Flow:

Authentication (Login) → Access Admin Dashboard → User Management (Customer/Vendor Accounts, Vendor Approval) → Product Moderation (Approve/Reject Products) → Category Management (CRUD operations) → Platform Overview.

📁 File Structure
The project is divided into client (React frontend) and server (Node.js/Express.js backend) directories, promoting modularity and separation of concerns.

/multi-vendor-marketplace
├── client/                      # React.js frontend application
│   ├── public/                  # Static assets
│   ├── src/                     # React source code
│   │   ├── components/          # Reusable UI components
│   │   ├── contexts/            # React Contexts for global state
│   │   ├── hooks/               # Custom React Hooks
│   │   ├── pages/               # Top-level page components (routes)
│   │   ├── services/            # API interaction logic
│   │   ├── utils/               # Utility functions
│   │   └── ...
├── server/                      # Node.js/Express.js backend API
│   ├── config/                  # Configuration files (DB, env)
│   ├── controllers/             # Business logic handlers
│   ├── middleware/              # Express middleware (auth, error, upload)
│   ├── models/                  # Mongoose schemas
│   ├── routes/                  # API endpoints
│   ├── utils/                   # Utility functions (JWT, validation, Stripe)
│   ├── uploads/                 # Temporary storage for uploaded files
│   ├── server.js                # Main server entry file
│   └── ...
├── .env                         # Root environment variables
├── .gitignore                   # Git ignore file
├── package.json                 # Project-level dependencies
└── README.md                    # Project documentation

⚙️ Setup & Installation
To get a local copy up and running, follow these steps.

Prerequisites
Node.js (v18 or higher recommended)

npm (comes with Node.js) or yarn

MongoDB (local instance or MongoDB Atlas account)

Stripe Account (for payment integration)

Backend Setup
Clone the repository:

git clone https://github.com/iamSunnyrohit/Marketplace.git
cd Marketplace/server

Install backend dependencies:

npm install
# or yarn install

Create a .env file in the server directory and add your environment variables:

PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=a_very_secret_key_for_jwt
STRIPE_SECRET_KEY=your_stripe_secret_key
# Add other necessary environment variables (e.g., cloud storage credentials if used)

Replace your_mongodb_connection_string with your MongoDB URI.

Replace a_very_secret_key_for_jwt with a strong, random string.

Replace your_stripe_secret_key with your actual Stripe secret key.

Start the backend server:

npm start
# or node server.js

The server should start on http://localhost:5000 (or your specified PORT).

Frontend Setup
Navigate to the client directory:

cd ../client

Install frontend dependencies:

npm install
# or yarn install

Create a .env file in the client directory and add your environment variables:

REACT_APP_API_URL=http://localhost:5000/api
REACT_APP_STRIPE_PUBLIC_KEY=your_stripe_publishable_key

Replace your_stripe_publishable_key with your actual Stripe publishable key.

Start the frontend development server:

npm start

The React app should open in your browser, typically at http://localhost:3000.

🚀 Usage
Customer: Register, log in, browse products, add to cart, proceed to checkout, view order history.

Vendor: Register (await admin approval), log in to the vendor dashboard, manage products, view and update orders.

Admin: Log in to the admin dashboard, manage users, approve vendors, moderate products, and oversee the platform.

🤝 Contributing
Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are greatly appreciated.

Fork the Project

Create your Feature Branch (git checkout -b feature/AmazingFeature)

Commit your Changes (git commit -m 'Add some AmazingFeature')

Push to the Branch (git push origin feature/AmazingFeature)

Open a Pull Request

📄 License
Distributed under the MIT License. See LICENSE for more information.