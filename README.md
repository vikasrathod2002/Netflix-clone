![Screenshot 2025-03-03 230938](https://github.com/user-attachments/assets/c500029d-2105-43a7-9373-931b5c6379fb)

🌐 Live Demo : https://netflix-clone-1-yw5j.onrender.com/

# 🎥 Netflix Clone - Full-Stack Streaming Platform 🌐

A **fully responsive, full-stack Netflix clone** built using **React.js, TailwindCSS, Node.js, Express.js, and MongoDB**. This project delivers an immersive streaming experience with **secure authentication, content browsing, trailer previews, actor searches, and personalized recommendations**. 

## 🚀 Tech Stack

| Technology     | Purpose                                               |
|----------------|-------------------------------------------------------|
| **React.js**   | Frontend development                                  |
| **TailwindCSS**| Modern responsive UI design                           |
| **Node.js**    | Backend runtime for server logic                      |
| **Express.js** | RESTful API creation                                  |
| **MongoDB**    | NoSQL database for user data & search history         |
| **JWT**        | Secure user authentication & authorization            |

---

## ✨ Key Features

✅ **User Authentication & Authorization**  
- Secure **JWT-based authentication** for user signup, login, and logout.
- **Auth-protected routes** for premium features.
- Password hashing using **bcrypt**.

✅ **Movie & TV Show Catalog**  
- Browse movies and TV shows by **categories** (trending, top-rated, genres).
- View **detailed information** for each movie or show, including synopsis, cast, and trailers.
- View **similar recommendations** to discover new content.

✅ **Advanced Search Features**  
- **Search by Title** — Find movies, TV shows, and actors.
- **Actor Search** — Discover content featuring a specific actor.
- **Search History Tracking** — Automatically save and display recent searches.

✅ **Trailer Previews**  
- Watch **official trailers** directly on the app.
- Integrated with reliable movie database APIs for up-to-date trailers.

✅ **Personalized Recommendations**  
- Dynamic recommendations based on **currently viewed content**.
- Explore **similar movies and shows** directly from the details page.

✅ **Responsive UI with TailwindCSS**  
- Fully responsive across **mobile, tablet, and desktop** devices.
- Styled with **TailwindCSS** for modern design & performance.

✅ **RESTful API Structure**  
- Clean and modular **controller-service-router** architecture.
- API routes to fetch movies, TV shows, trailers, and search history.

---

## 🗂️ Folder Structure

    /
    |-- client/                     # Frontend (React + Tailwind)
    |   |-- src/                     # Source code
    |   |   |-- components/          # Reusable UI components (Buttons, Cards, etc.)
    |   |   |-- pages/                # Pages like Home, Search, Movie Details
    |   |   |-- services/             # API call functions (Axios services)
    |   |   |-- App.js                # Main React application entry point
    |   |-- public/                   # Static assets (favicon, icons, etc.)
    |   |-- package.json              # Frontend dependencies & scripts

    |-- server/                      # Backend (Node.js + Express.js)
    |   |-- controllers/              # Business logic & data handling functions
    |   |-- routes/                   # API route definitions
    |   |-- models/                   # Mongoose schemas (e.g., User, Snippet)
    |   |-- middleware/               # JWT authentication & authorization middleware
    |   |-- utils/                     # Utility/helper functions
    |   |-- config/                    # Database connection & app configuration
    |   |-- server.js                  # Main backend entry point
    |   |-- package.json               # Backend dependencies & scripts

    |-- .env                          # Environment variables (excluded via .gitignore)
    |-- .gitignore                    # Files & directories to be ignored by Git
    |-- README.md                     # Project documentation 

📌 Explanation Table 

    Path	Description
    /client	                        Contains the frontend code (React + Tailwind).
    /client/src/components	        Reusable UI components like buttons, cards, modals, etc.
    /client/src/pages	              Page components (Home, Search, Movie Details, etc.).
    /client/src/services 	          Service functions for API calls using Axios.
    /server	                        Contains the backend code (Node.js + Express.js).
    /server/controllers	            Business logic functions that handle requests and responses.
    /server/routes	                API endpoints (e.g., /api/snippets, /api/auth).
    /server/models	                MongoDB schemas/models using Mongoose.
    /server/middleware            	Middleware like JWT authentication.
    /server/utils	                  Helper functions like token handling, data validation, etc.
    /server/config	                Configuration files (DB connection, environment variables).
    /server/server.js	              Main entry file to start the backend server.
    .env	                          Environment variables file (DB URI, JWT secret, etc.).
    .gitignore	                    Defines files/folders that Git should ignore.
    README.md	                      Documentation file for the project.

---

## 🔐 Authentication & Security

- **JWT Authentication** — Secure user login with **HTTP-Only Cookies**.
- **Bcrypt Password Hashing** — Strong encryption for user passwords.
- **Auth Middleware** — Protect sensitive routes using `protectRoute` middleware.
- **CORS Configuration** — Secure cross-origin requests between frontend & backend.

---

## 🔥 Core API Endpoints (Backend)

### Auth Routes

| Endpoint         | Method | Description                 |
|------------------|-------|-----------------------------|
| `/api/auth/signup`   | POST | Register new user          |
| `/api/auth/login`    | POST | Login user                  |
| `/api/auth/logout`   | POST | Logout user                 |
| `/api/auth/authCheck`| GET  | Check if user is authenticated (protected) |

---

### Movie Routes

| Endpoint                     | Method | Description                          |
|------------------------------|-------|--------------------------------------|
| `/api/movies/trending`       | GET   | Fetch trending movies                |
| `/api/movies/:id/trailers`   | GET   | Get trailers for a movie              |
| `/api/movies/:id/details`    | GET   | Fetch movie details                   |
| `/api/movies/:id/similar`    | GET   | Get similar movies                    |
| `/api/movies/:category`      | GET   | Fetch movies by category (genres etc.)|

---

### TV Show Routes

| Endpoint                     | Method | Description                          |
|------------------------------|-------|--------------------------------------|
| `/api/tv/trending`          | GET   | Fetch trending TV shows              |
| `/api/tv/:id/trailers`      | GET   | Get trailers for a TV show            |
| `/api/tv/:id/details`       | GET   | Fetch TV show details                 |
| `/api/tv/:id/similar`       | GET   | Get similar TV shows                  |
| `/api/tv/:category`         | GET   | Fetch TV shows by category            |

---

### Search Routes

| Endpoint                     | Method | Description                          |
|------------------------------|-------|--------------------------------------|
| `/api/search/person/:query` | GET   | Search for actors                     |
| `/api/search/movie/:query`  | GET   | Search for movies                     |
| `/api/search/tv/:query`     | GET   | Search for TV shows                   |
| `/api/search/history`       | GET   | Get user search history               |
| `/api/search/history/:id`   | DELETE| Remove item from search history       |

## 📥 Installation & Setup
Install Dependencies
# Backend dependencies
    cd server
    npm install

# Frontend dependencies
    cd  client
    npm install

# Environment Variables 
    MONGO_URI=mongodb_connection_string
    JWT_SECRET=jwt_secret
    PORT=5000
    TMDB_API_KEY=rhdhdhdhey764673
# Run the App
    cd server
    npm run dev

# Frontend
    cd  client
    npm run dev
🔗 Contact

Email: vikassrathod2002@gmail.com
    
