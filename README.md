# 📚 Goodreads Clone - Backend (goodreads-node)

A **Node.js + Express.js Backend** for a Goodreads-style book management system. This API allows users to **browse books, manage collections, leave reviews, authenticate using JWT, and interact with a digital library**.

---

## 🚀 Features

✅ **User Authentication** (JWT-based login, Google OAuth)  
✅ **Admin Dashboard** (Manage users, books, authors, and categories)  
✅ **Books & Authors** (CRUD operations, search, filtering)  
✅ **User Reviews & Ratings** (Rate and review books)  
✅ **Subscription Management** (Stripe-powered payment system)  
✅ **Google Drive Integration** (For storing book PDFs)  
✅ **Secure API** (Token-based authentication, role-based access)  

---

## 🏷️ Project Structure

```
📂 goodreads-node
 ├── controllers/        # API controllers
 ├── middleware/         # Authentication & authorization
 ├── models/             # Mongoose schemas
 ├── routes/             # API routes
 ├── scripts/            # Utility scripts (e.g., admin setup)
 ├── utils/              # Helper functions (e.g., JWT, email, uploads)
 ├── views/              # Static files
 ├── app.js              # Main Express application
 ├── package.json        # Dependencies & scripts
```

---

## 🔧 Installation & Setup

### **1️⃣ Clone the Repository**
```sh
git clone git@github.com:OmarSameh2001/goodreads-node.git
cd goodreads-node
```

### **2️⃣ Install Dependencies**
```sh
npm install
```

### **3️⃣ Configure Environment Variables**
- Create a `.env` file inside `goodreads-node` and add:
  ```
  MONGO_CONNECTION_STRING=your_mongo_url
  JWT_SECRET=your_jwt_secret
  JWT_EXPIRES_IN=6h
  STRIPE_SECRET_KEY=your_stripe_key
  GOOGLE_CLIENT_ID=your_google_client_id
  GOOGLE_CLIENT_SECRET=your_google_client_secret
  IMGUR_CLIENT_ID=your_imgur_client_id
  EMAIL_USER=your_email@example.com
  EMAIL_PASS=your_email_password
  ```

### **4️⃣ Start the Server**
```sh
npm start
```
🚀 Your API will be running at **http://localhost:3001**

---

## 📌 API Endpoints

### **Authentication**
| Method | Endpoint         | Description |
|--------|-----------------|-------------|
| POST   | `/auth/register` | Register a new user |
| POST   | `/auth/login` | User login |
| POST   | `/auth/google/callback` | Google OAuth login |
| POST   | `/auth/verify-otp` | Verify OTP sent via email |
| POST   | `/auth/renew-subscription/:id` | Renew user subscription |

### **Books**
| Method | Endpoint           | Description |
|--------|-------------------|-------------|
| GET    | `/books/`         | Get all books |
| GET    | `/books/:id`      | Get a single book |
| POST   | `/books/`         | Create a new book (Admin) |
| PUT    | `/books/:id`      | Update a book (Admin) |
| DELETE | `/books/:id`      | Delete a book (Admin) |

### **Authors**
| Method | Endpoint          | Description |
|--------|------------------|-------------|
| GET    | `/authors/`      | Get all authors |
| GET    | `/authors/:id`   | Get a specific author |
| POST   | `/authors/`      | Create a new author (Admin) |
| PUT    | `/authors/:id`   | Update an author (Admin) |
| DELETE | `/authors/:id`   | Delete an author (Admin) |

### **User Interactions**
| Method | Endpoint                 | Description |
|--------|-------------------------|-------------|
| POST   | `/userBook/`            | Add a book to user’s collection |
| PATCH  | `/userBook/review/:bookId` | Add a book review |
| PATCH  | `/userBook/rate/:bookId` | Rate a book |
| DELETE | `/userBook/:id`         | Remove a book from collection |

### **File Uploads (Google Drive)**
| Method | Endpoint      | Description |
|--------|--------------|-------------|
| POST   | `/upload/`   | Upload a book PDF to Google Drive |

---

## 💡 Tech Stack
| Backend  | Database | APIs |
|----------|----------|----------|
| Node.js  | MongoDB  | Stripe API |
| Express  | Mongoose | Google Drive API |
| JWT Auth |          | Nodemailer |

---

## 🛡 Security Considerations
- **JWT Authentication** for secure API access.
- **Environment Variables** for sensitive credentials (`.env` file).
- **Role-Based Access Control (RBAC)** for user & admin management.
- **Rate Limiting & Validation** for API protection.

---

## 📌 Future Improvements
- 📈 **GraphQL Support for Better Queries**
- 🌍 **AI-Powered Book Recommendations**
- 📊 **Advanced Logging & Monitoring**
- 🎯 **Improved API Rate Limiting for Security**

---

## 🏗 Contributing

👉 Fork the repository  
👉 Create a feature branch (`git checkout -b feature-branch`)  
👉 Commit your changes (`git commit -m "Added new feature"`)  
👉 Push to the branch (`git push origin feature-branch`)  
👉 Open a Pull Request 🚀  

---

## 🐝 License
This project is licensed under the MIT License.

---

## 👨‍💻 Author
- **Your Name** - [GitHub](https://github.com/your-username)
```

