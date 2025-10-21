# 🚗 Car Rental System (MERN Stack)

A comprehensive **Car Rental Web Application** built using the **MERN stack (MongoDB, Express.js, React.js, Node.js)**.  
This platform enables customers to browse, book, and manage car rentals seamlessly — while providing administrators with tools to oversee vehicles, users, and bookings.

---

## 🌟 Overview

This project is designed to replicate a modern **car rental management platform**. It provides a full end-to-end experience — from user authentication and booking to admin-level control and analytics — demonstrating how frontend, backend, and database layers interact in a real-world application.

---

## 🧩 Tech Stack

| Category | Technology |
|-----------|-------------|
| Frontend | React.js, Axios, Bootstrap / Material UI |
| Backend | Node.js, Express.js |
| Database | MongoDB with Mongoose |
| Authentication | JSON Web Token (JWT) |
| State Management | React Hooks / Context API |
| API Architecture | RESTful |
| Deployment Ready | Fully configurable with environment variables |

---

## ⚡ Key Highlights

- 🔒 **JWT Authentication:** Secure login and protected routes for users and admins.  
- 🧠 **Scalable Architecture:** Clean separation of backend routes, controllers, and models.  
- ⚙️ **Dynamic Filtering:** Users can filter available cars based on type, price, or date.  
- 🧾 **Booking Validation:** Prevents overlapping bookings using date validation logic.  
- 📱 **Responsive Frontend:** Optimized layout for mobile, tablet, and desktop users.  

---

## 👥 User Features (Customer Side)

### 🧍‍♂️ 1. User Registration and Login
- Users can sign up and log in using their email and password.
- Passwords are hashed using **bcrypt** before being stored.
- Once authenticated, users receive a **JWT token** stored securely in local storage.
- Protected pages (like booking history) require valid tokens for access.

### 🚘 2. Browse and View Cars
- Users can browse all available cars fetched dynamically from MongoDB.
- Each car card displays:
  - Car image  
  - Model name  
  - Price per day  
  - Description  
  - Booking availability  
- Car listings update automatically when admins add or modify cars.

### 📅 3. Book a Car
- Users can select rental start and end dates.
- The system checks car availability for the chosen time window.
- Once confirmed, the booking is stored in the database with:
  - User ID  
  - Car ID  
  - Duration  
  - Total cost  

### 🧾 4. Manage and View Bookings
- Each user can view all their current and past bookings.
- Bookings display:
  - Car details  
  - Dates of rental  
  - Total amount paid  
  - Booking status  
- Users can cancel bookings before the start date (if enabled).

### 💳 5. Secure Payments *(Optional / Extensible)*
- Placeholder logic ready for integration with **Stripe** or **Razorpay** APIs.
- Once integrated, users can complete bookings using secure online payments.

---

## 🛠️ Admin Features (Management Side)

### 👨‍💼 1. Admin Authentication
- Separate login for admin users with elevated privileges.
- Admin dashboard is protected and accessible only with a valid **JWT token** and admin role flag.

### 🚗 2. Car Management
- Admins can **add new cars** with full details: name, model, price, image, fuel type, transmission, etc.
- Cars can be **edited** or **deleted** dynamically.
- Backend validates required fields before saving cars to the MongoDB collection.

### 📋 3. Booking Management
- Admins have a dashboard to view **all bookings** in the system.
- Each booking displays:
  - Customer details  
  - Car details  
  - Dates of booking  
  - Total payment  
  - Booking status  
- Admins can manually **approve**, **reject**, or **cancel** bookings if required.

### 📊 4. Dashboard Overview
- Quick summary of system data such as:
  - Total registered users  
  - Total cars listed  
  - Active bookings  
  - Cars currently available  

### 🔔 5. Real-Time Data Sync
- Admin changes (like car addition/deletion) instantly reflect on the user interface via dynamic API updates.

---

## 🔐 Authentication & Authorization System

1. **Registration Process**
   - User submits credentials → password is hashed → stored in MongoDB.  
2. **Login Process**
   - Credentials are verified; upon success, a **JWT token** is issued.  
3. **Protected Routes**
   - Backend validates the JWT before processing sensitive requests.  
   - Admin routes verify both authentication and admin privileges.  
4. **Logout**
   - Client simply removes the token from local storage, ending the session.  

---

## 🧠 Backend Logic (Express + MongoDB)

- The backend follows a **Model-Controller-Route (MCR)** architecture:
  - **Models**: Define Car, User, and Booking schemas via Mongoose.
  - **Controllers**: Handle core logic (CRUD, validation, authentication).
  - **Routes**: Map API endpoints for clean access via `/api/cars`, `/api/bookings`, `/api/users`.

- Key APIs include:
  - `POST /api/users/register` – Register a new user  
  - `POST /api/users/login` – Authenticate and return JWT  
  - `GET /api/cars` – Fetch all cars  
  - `POST /api/bookings` – Book a car  
  - `GET /api/bookings/user/:id` – Get all bookings by a user  

---

## 💻 Frontend Logic (React)

- React handles UI state and routing via **React Router**.
- Components include:
  - `Home.js` – Car listings  
  - `Login.js` / `Register.js` – Authentication forms  
  - `Booking.js` – Car booking flow  
  - `AdminDashboard.js` – Admin panel and analytics  
- Axios handles API requests, while local storage keeps user tokens persistent across reloads.

---

## 🛡️ Security & Data Integrity

- **bcrypt** ensures passwords are stored securely.  
- **JWT** tokens prevent unauthorized access.  
- **CORS** and **Helmet** middleware protect API endpoints.  
- All critical actions (like booking creation or car updates) are validated server-side.  

---

## 📈 Future Enhancements

- 💳 **Online Payments:** Integrate Stripe or Razorpay for live payments.  
- 🌐 **Deployment:** Deploy to Render, Vercel, or AWS with MongoDB Atlas.  
- 📧 **Email Notifications:** Notify users of booking confirmations or cancellations.  
- 📊 **Analytics Dashboard:** Add charts for booking trends and revenue insights.  
- 🗺️ **Location Integration:** Filter cars by pickup/drop-off cities using Google Maps API.  
- 🧠 **AI-based Pricing:** Dynamic pricing based on demand and duration.  

---

## 🤝 Contributing

Contributions are welcome!  
Fork the repository, create a new branch for your feature or fix, and submit a pull request.

---

## 📄 License

This project is licensed under the **MIT License** — you’re free to use, modify, and distribute it.

---

## 💬 Contact

**Developer:** Aditeey Singh Jadon  
📧 [aditeeysinghjadon@gmail.com](mailto:aditeeysinghjadon@gmail.com)  
🔗 [GitHub Profile](https://github.com/AditeeySingh)
