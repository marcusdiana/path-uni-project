# Mentoring Platform

A full-stack web application that connects secondary school female students with women professionals from various industries, providing free career support and mentoring to aid in career development from a young age.

## Purpose

This platform was designed to give young women the opportunity to gain a better understanding of the many career paths available to them, allowing them to make more informed decisions about their future. The application facilitates meaningful connections between mentors and mentees through real-time communication features.

## Features

- **User Authentication**: Secure registration and login system with JWT tokens
- **Role-Based Access**: Support for mentors, mentees, and admin roles
- **Real-Time Chat**: Live messaging functionality powered by Socket.io
- **User Dashboard**: Personalized dashboard for logged-in users
- **Search Functionality**: Find and connect with mentors/mentees
- **Responsive Design**: Modern UI built with Bootstrap and custom CSS

## Tech Stack

### Frontend
- **React** 18.0.0 - UI library
- **React Router** 6.3.0 - Client-side routing
- **Socket.io Client** 4.5.0 - Real-time communication
- **Bootstrap** 5.1.3 - CSS framework
- **React Bootstrap** 2.3.0 - Bootstrap components for React
- **Axios** 0.26.1 - HTTP client

### Backend
- **Node.js** - Runtime environment
- **Express** 4.17.3 - Web framework
- **Socket.io** 4.5.0 - Real-time bidirectional communication
- **MongoDB** 4.5.0 - Database
- **Mongoose** 6.3.1 - MongoDB object modeling
- **JWT** 8.5.1 - Authentication tokens
- **Bcryptjs** 2.4.3 - Password hashing

## Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (version 14 or higher recommended)
- **npm** (comes with Node.js)
- **MongoDB** (local installation or MongoDB Atlas account)

### 1. Clone the Repository

```bash
git clone <your-repo-url>
cd path-uni-project
```

### 2. Server Setup

Navigate to the server directory and install dependencies:

```bash
cd server
npm install
```

Create a `.env` file in the `server` directory:

```env
MONGO_URL=
JWT_SECRET=
JWTEXPIRE=
```

Start the server:

```bash
npm run dev
```

The server will run on `http://localhost:5000` (or the port specified in your `.env` file).

### 3. Client Setup

Open a new terminal, navigate to the client directory, and install dependencies:

```bash
cd client
npm install
```

Start the React development server:

```bash
npm start
```

The client will run on `http://localhost:3000` and automatically open in your browser.

## Project Structure

```
path-uni-project/
├── client/                 # React frontend application
│   ├── public/            # Static files
│   ├── src/
│   │   ├── components/    # React components
│   │   │   ├── ChatRoom.js
│   │   │   ├── Login.jsx
│   │   │   ├── Register.jsx
│   │   │   └── ...
│   │   ├── css/          # Stylesheets
│   │   ├── header/       # Navigation components
│   │   └── index.js      # Entry point
│   └── package.json
│
├── server/                # Express backend
│   ├── controllers/      # Request handlers
│   ├── database/         # Database connection
│   ├── middleware/       # Custom middleware (auth, error handling)
│   ├── models/           # Mongoose schemas
│   ├── routes/           # API routes
│   ├── utils/            # Utility functions
│   ├── index.js          # Server entry point
│   └── package.json
│
└── README.md
```

## Troubleshooting

### Server Issues

**"Could not connect database!"**
- Ensure MongoDB is running (if using local MongoDB)
- Verify your `MONGO_URL` in the `.env` file
- For MongoDB Atlas, ensure your IP is whitelisted

**Port already in use**
- Change the `PORT` in your `.env` file
- Update `client/src/setupProxy.js` to match the new port

### Client Issues

**Proxy errors**
- Ensure the server is running
- Verify the port in `client/src/setupProxy.js` matches your server port

**Build errors**
- Delete `node_modules` and `package-lock.json`
- Run `npm install` again

## Notes

- This project uses JWT for authentication
- Real-time chat functionality is powered by Socket.io
- The application supports three user roles: mentor, mentee, and admin
- Passwords are hashed using bcryptjs before storage




---

Built with ❤️ to empower young women in their career journeys.
