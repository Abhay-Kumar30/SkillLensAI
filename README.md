# SkillLensAI    

[![Live App](https://img.shields.io/badge/Live-App-brightgreen)](https://resume-analyser-kp0f.onrender.com/)

## Description

- Designed and developed a scalable full-stack web application for AI-based resume analysis and evaluation.
- Built RESTful APIs using Spring Boot to handle resume uploads, user management, and analysis workflows.
- Integrated Google Gemini AI to extract skills, analyze resume content, and generate intelligent improvement suggestions.
- Implemented JWT-based authentication, email verification, and secure password reset flows using Brevo.
- Developed responsive and reusable React components for seamless user interaction and real-time insights.
- Used MySQL to manage user profiles, resume data, and analysis results with efficient relational mapping.
- Followed clean layered architecture and best practices to ensure maintainability and scalability.
- Tested APIs using Postman and managed version control using Git & GitHub.
- Collaborated using Agile development practices, focusing on clean, testable, and efficient code.

## Tech Stack
- Frontend: React.js | HTML5 | CSS3 | JavaScript (ES6+)
- Backend: Java | Spring Boot | RESTful APIs | JWT Authentication
- Database: MySQL (Relational Database)
- AI Integration: Google Gemini AI
- Security & Auth: JWT | Email Verification | Password Reset (Brevo)
- Tools & Practices: Git | GitHub | Postman | Agile Development
- Architecture: Layered Architecture (Controller, Service, Repository)

## Frontend & Backend Integration Notes

- The frontend UI is developed using **React**
- For deployment, the React application is **built and served by the Spring Boot backend** as static files
- The React production build files are placed inside the backend’s **static** directory

### Static & Template Files
- The `static` folder contains the **React production build files**
- The `templates` folder inside `static` is used to store **email templates**
  - Used for **email verification** and **password reset**

Thank you.
