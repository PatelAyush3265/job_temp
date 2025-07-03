JobConnect – MERN-Based AI Resume Screening Portal
JobConnect is a modern, full-stack web application designed to streamline the hiring process. It connects job seekers with employers, and leverages AI to automatically screen and rank resumes based on job descriptions.

Features
Dual User Roles: Separate interfaces and functionalities for Job Seekers and Employers.
User Authentication: Secure JWT-based authentication for registration and login.
Job Management: Employers can post, update, view, and delete job listings.
Job Browsing & Search: Job seekers can browse and filter jobs by title, country, and city.
AI-Powered ATS: Automatic resume screening using the Google Gemini API to score applicants based on skills and experience.
Application System: Job seekers can apply for jobs by uploading their resumes.
Real-time Chat: Integrated chat system using Socket.IO for communication between employers and applicants.
Applicant Shortlisting: Employers can shortlist promising candidates.
User Profiles: Users can view and update their profile information.
Dashboard Analytics: Employers can view a chart of ATS scores for their job applicants.
Tech Stack
Frontend: React, Vite, Tailwind CSS, Axios, Socket.IO Client, Chart.js
Backend: Node.js, Express.js, MongoDB (with Mongoose), JWT, Socket.IO, Google Gemini API
Database: MongoDB Atlas
File Storage: Supabase Storage
Project Setup
Prerequisites
Node.js (v14 or later)
npm
Git
A MongoDB Atlas account
A Supabase account (for file storage)
A Google AI Studio API Key (for Gemini)
Backend Setup
Clone the repository:

git clone <repository-url>
cd job_portal_cursor
Navigate to the backend directory:

cd backend
Install dependencies:

npm install
Create a .env file in the backend directory and add the following environment variables:

PORT=4000
FRONTEND_URL=http://localhost:5173
DB_URL=<your_mongodb_atlas_connection_string>
JWT_SECRET_KEY=<your_jwt_secret_key>
JWT_EXPIRE=7d
COOKIE_EXPIRE=7
NODE_ENV=development
SUPABASE_URL=<your_supabase_project_url>
SUPABASE_ANON_KEY=<your_supabase_anon_key>
GEMINI_API_KEY=<your_gemini_api_key>
Start the backend server:

npm start
The server should now be running on http://localhost:4000.

Frontend Setup
Navigate to the frontend directory:

cd ../frontend
Install dependencies:

npm install
Start the frontend development server:

npm run dev
The frontend should now be running on http://localhost:5173.

Deployment
Backend (Render)
Push your code to a GitHub repository.
Go to Render and create a new "Web Service".
Connect your GitHub repository.
Set the Build Command to npm install.
Set the Start Command to npm start.
Add all the necessary environment variables from your .env file in the "Environment" section.
Deploy the service.
Frontend (Vercel)
Push your code to a GitHub repository.
Go to Vercel and create a new project.
Connect your GitHub repository.
Vercel will automatically detect that it's a Vite project and configure the build settings.
No environment variables are needed for the frontend.
Deploy.
This README provides a comprehensive guide to getting JobConnect up and running.
