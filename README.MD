# Career Connect

Career Connect is a web application designed to help users find jobs that match their skills and preferences. It provides a robust platform for job seekers to manage their profiles and an administrative interface to manage categories, skills, and educations.

## Tech Stack

### Frontend
- **Framework:** [Angular 17](https://angular.io/)
- **Styling:** [Tailwind CSS](https://tailwindcss.com/) & [Angular Material](https://material.angular.io/)
- **Authentication:** [Firebase Auth](https://firebase.google.com/docs/auth)

### Backend
- **Environment:** [Node.js](https://nodejs.org/) & [Express](https://expressjs.com/)
- **Database:** [MongoDB](https://www.mongodb.com/) (using [Mongoose](https://mongoosejs.com/))
- **Other:** Webpack for bundling

## Project Structure

- `/client/career-connect-web` - Contains the Angular frontend application.
- `/backend` - Contains the Express backend API.
- `/hard-config` - Contains scripts to seed the database or manage Firebase admin tasks.

## Getting Started

### Prerequisites
- [Node.js](https://nodejs.org/)
- [Docker](https://www.docker.com/) (to easily run a local MongoDB instance)
- [Angular CLI](https://angular.io/cli)

### Running the Application Locally

1. **Start MongoDB:**
   You can quickly spin up a MongoDB instance using Docker:
   ```bash
   docker run -d -p 27017:27017 --name mongo-career-connect mongo
   ```

2. **Run the Backend:**
   Open a terminal and navigate to the backend directory.
   ```bash
   cd backend
   npm install
   npm start
   ```
   The API will be available at `http://localhost:3000`.

3. **Run the Frontend:**
   Open another terminal and navigate to the frontend directory.
   ```bash
   cd client/career-connect-web
   npm install
   npm start
   ```
   The application will be available at `http://localhost:4200`.

## Signing In

To access the platform, you can either create a new user account through the "Register" page on the application, or you can use the predefined administrator account to access the admin dashboard.

**Admin Credentials:**
- **Email:** `admin@example.com`
- **Password:** `123456`

*(Note: If you ever need to recreate the admin account, you can do so by running `node firebase-admin-config.js` inside the `/hard-config` directory.)*

## Features

- **User Registration/Login:** Secure authentication powered by Firebase.
- **Profile Management:** Manage your educational background, skills, and job preferences (Remote, On-site, Hybrid, Government, Non-Government).
- **Admin Dashboard:** Administrators can manage categories, skills, educational options, and platform notifications.

---
*Happy connecting!*