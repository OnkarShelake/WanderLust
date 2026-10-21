# 🏡 WanderLust - Travel & Accommodation Listing Platform

WanderLust is a full-stack web application inspired by accommodation and travel listing platforms. It allows users to explore, create, edit, and delete property listings, upload listing images, add reviews, and locate properties using an interactive map.

The project is built using **Node.js, Express.js, MongoDB, Mongoose, EJS, Cloudinary, and Mapbox**.

---

## 🚀 Live Demo

🔗 Live Website: `https://wanderlust-qc6r.onrender.com/`

🔗 GitHub Repository: `https://github.com/OnkarShelake/WanderLust`

---

## 📌 Features

### 👤 User Authentication
- User registration and login
- Secure password authentication using Passport.js
- Login/logout functionality
- Session management
- Flash messages for user feedback

### 🏠 Listing Management
- View all accommodation listings
- View individual listing details
- Create new listings
- Edit existing listings
- Delete listings
- Owner-based authorization
- Listing validation using Joi

### 🖼️ Image Upload
- Upload listing images
- Images are stored in **Cloudinary**
- Cloudinary URL and filename are stored in MongoDB
- Supports image replacement when editing listings

### ⭐ Review & Rating System
- Users can add reviews
- Users can provide star ratings
- Reviews are displayed on listing pages
- Review authors are associated with their reviews
- Review deletion with authorization

### 🗺️ Map Integration
- Integrated **Mapbox API**
- Displays listing location on an interactive map
- Helps users understand where the property is located

### 🔐 Authorization
- Only authenticated users can create listings and reviews
- Only listing owners can edit/delete their listings
- Review authors can delete their own reviews

### 🔎 Search & Categories
- Search interface for listings
- Category/filter UI for different types of properties

### ☁️ Cloud Deployment
- Application can be deployed on **Render**
- Source code is maintained using Git and GitHub
- Environment variables are used for sensitive credentials

---

# 🛠️ Tech Stack

## Frontend

- HTML
- CSS
- JavaScript
- Bootstrap
- EJS
- Font Awesome

## Backend

- Node.js
- Express.js

## Database

- MongoDB
- Mongoose

## Authentication

- Passport.js
- Passport Local
- Passport Local Mongoose
- Express Session
- Connect Mongo

## Image Storage

- Cloudinary
- Multer
- Multer Storage Cloudinary

## Maps

- Mapbox API

## Validation

- Joi

## Other Tools

- Git
- GitHub
- Nodemon
- Dotenv
- Method Override
- Connect Flash
- EJS Mate

---

# 🏗️ Project Architecture

```text
                    ┌─────────────────────┐
                    │       Browser       │
                    │   HTML/CSS/JS/EJS   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │     Express.js      │
                    │       Server        │
                    └──────────┬──────────┘
                               │
             ┌─────────────────┼─────────────────┐
             │                 │                 │
             ▼                 ▼                 ▼
       ┌───────────┐     ┌────────────┐    ┌────────────┐
       │   Routes  │     │ Middleware │    │ Controllers│
       └─────┬─────┘     └─────┬──────┘    └─────┬──────┘
             │                 │                 │
             └─────────────────┼─────────────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │      Mongoose       │
                    │       Models        │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │       MongoDB       │
                    │       Database       │
                    └─────────────────────┘

        External Services
        ───────────────────────────────

        Cloudinary  → Listing Images
        Mapbox      → Location & Maps
